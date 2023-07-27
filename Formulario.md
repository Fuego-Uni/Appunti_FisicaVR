
old patter: ```/( ?\`$\$(.|\n)*?\$\$)|(#formul[a] ?(.*))/g;```


```dataviewjs
const PATTERN = /(> \[!formula\] .*\n> \$\$(.|\n)*?\$\$)|(> \[!formula\] .*(\n>.*)*)/g;

let collectedFormulas = {};

// Get all files in the vault
let files = dv.app.vault.getMarkdownFiles();

for (let file of files) {
  if (file.name == 'Formulario.md') { continue }
  
  let content = await dv.app.vault.cachedRead(file);

  // Get the lines with the formula tag
  let matches = content.matchAll(PATTERN);
  
  for (let match of matches) {
    let file_link = `[[${file.name}]]`
    let formula = `${match[0]}`.replace('' + ' ', '');

    // initialise an array for the file if it does not exist yet
    if(!collectedFormulas[file_link]) {
      collectedFormulas[file_link] = [];
    }

    // then push the formula into the array
    collectedFormulas[file_link].push(formula);
  }
}

// prepare output
let output = '';
for (let file_link in collectedFormulas) {
  output += `**${file_link}**: \n`
  for(let formula of collectedFormulas[file_link]) {
    output += `- ${formula}\n`;
  }
  output += '\n';
}

dv.paragraph(output);

```