# Data Experiment Traps: Biases, Fallacies, Malpractice, and Heuristics

![sampleImage](sample-edited/edited-sampleImage.png)

## To Run

Tested on Ubuntu

```shell
# Optional but recommended
# Version lasted tested was node v16.16.0 (npm v8.11.0)
nvm use --lts
```

```shell
npm install # or npm i
```

```
npx parcel index.html
```

When done `Ctrl+C` in terminal

## To Edit

Hint: 
- Bulk of editing is in [data.json](https://github.com/pkiage/research-contribution/blob/master/data.json) and in vector graphic editor
- [data.json](https://github.com/pkiage/research-contribution/blob/master/data.json) editing will help give initial SVG for further editing
- SVG from just `npx parcel index.html`  most likely requires further editing in vector graphic editor

### Data used in Algorithmic Design

Change name and children in [data.json](https://github.com/pkiage/research-contribution/blob/master/data.json)

### SVG

#### Obtain

#### Print

Print page (landscape layout) and open in application such as Adobe Illustrator

##### Browser Extention
Obtain SVG from web page using software ([SVGExport.io](https://svgexport.io/), [SVG Gobbler](https://github.com/rossmoody/svg-gobbler) etc.)

##### Inspect Element

1. Inspect Element `fn + f12`
2. Copy SVG contained in body class main

### SVG Further edits

For further edits export as SVG to edit in various vector graphic editors (Adobe Illustrator, BoxySVG, LibreOffice - Draw, Inkscape etc.)

Consider adding assets created/edited in other software (Adobe Creative Cloud, Canva, Figma, Microsoft Office etc.)

#### Tips

- Change colors from [style.css](https://github.com/pkiage/data-experiments-traps-viz/blob/master/style.css) or vector editing software
- If coloring in vector software e.g. Adobe Illustrator
    - For text and shapes fill 
    - For lines fill stroke
    - To select multiple either in Adobe Illustrator either use direct selection tool or press shift while selecting
- Ctrl + or Ctrl - to zoom out and in respectively
- SVG from browswer extention preferable because from pdf tends to create letters to outlines rather than editable text ([source](https://community.adobe.com/t5/illustrator-discussions/imported-svg-but-can-t-change-text/td-p/12739931))
- Bulk edit fonts in Adobe Illustrator
    - Font: `Type > Find/Replace Font... > Change all`

## Inspiration

### Concept & Implementation

- [pkiage research-contribution-semantic-strategies-viz Github Repository](https://github.com/pkiage/research-contribution-semantic-strategies-viz)


#### Accessibility

Color:
- [Adobe Color](https://color.adobe.com/create/color-accessibility)
- [Color Brewer 2.0](https://colorbrewer2.org/#type=qualitative&scheme=Dark2&n=3)
    - `#7570b3`
    - `#d95f02`
    - `#1b9e77`
- [Colour me better: fixing figures for colour blindness](https://www.nature.com/articles/d41586-021-02696-z)
- [Colorgorical](http://vrl.cs.brown.edu/color)
- [i want hue](https://medialab.github.io/iwanthue/)

Font:
- [Designing Effective Scientific Presentations](https://www.ibiology.org/professional-development/scientific-presentations/)
- Sans Serif font e.g. Trebuchet MS
- Bulk edit
    - Select text from layers (select multiple by press Ctrl while selecting)
    - Change position if necessary
    - Type > Size > (select ideal font size)

### Data

DYOR :)

- [Category:Cognitive biases](https://en.wikipedia.org/wiki/Category:Cognitive_biases)
- [Category:Heuristics](https://en.wikipedia.org/wiki/Category:Heuristics)
- [List of cognitive biases](https://en.wikipedia.org/wiki/List_of_cognitive_biases)
- [List of fallacies](https://en.wikipedia.org/wiki/List_of_fallacies)
- [Misuse of statistics](https://en.wikipedia.org/wiki/Misuse_of_statistics)

## Fixes if "To Run" has errors

### Update Node

```shell
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -

sudo apt-get install -y nodejs
```

### Install nvm

```shell
sudo apt-get install curl

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

Close then open terminal for changes to reflect

Verify installation

```shell
# should return nvm
command -v nvm

# should return version
nvm --version

# should list versions of Node currently installed
nvm ls
```

### Install current and stable LTS versions of Node.js

```shell
# list all versions of Node.js available
nvm ls-remote
```

```shell
# current stable LTS release of Node.js (production apps)
nvm install --lts

# current release of Node.js (testing latest features)
nvm install node

# install specific version
# nvm install version
# Example version = v17.0.0
nvm install v17.0.0
```

Verify installation

```shell
nvm ls

node --version # or which node

npm --version # or which npm
```

### Specify version of Node to use

Current release of Node.js (testing latest features)

```shell
nvm use node
```

Current stable LTS release of Node.js (production apps)

```shell
nvm use --lts
```

Specify version

```shell
# nvm use version
# Example version = v17.0.0
nvm use v17.0.0
```

### Fixes References

- [How To Install Node.js on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04)
- [npm does not support Node.js v10.19.0](https://askubuntu.com/questions/1382565/npm-does-not-support-node-js-v10-19-0)
- [Parcel js can't run same project on Ubuntu](https://stackoverflow.com/questions/68801380/parcel-js-cant-run-same-project-on-ubuntu)
- [Solve - nvm: command not found error](https://bobbyhadz.com/blog/nvm-command-not-found)

## Folder Structure

```folder-structure 
├── sample-edited                         ### Folder containing samples of raw SVG edited in vector processing software
|    ├── edited-sampleDocument.svg        ### Sample edited SVG saved as PDF (for best view in Github look at PNG since PDF might be distorted during rendering)
|    ├── edited-sampleImage.svg           ### Sample edited SVG exported as PNG with white background
|    └── edited-sampleSVG.svg             ### Sample edited SVG
├── sample-raw                            ### Folder containing samples of raw SVG obtained from running `npx parcel index.html`
|    ├── raw-browserExtentionExtract.svg  ### Raw export of SVG extrated from browser extension before further edits
|    ├── raw-PDFillustratorExtract.svg    ### Raw export of SVG obtained from saving PDF obtained from browser then opening in Adobe Illustrator then saving as SVG
|    └── raw-printPDF.svg                 ### Raw export of PDF printed from browser
|
├── .gitignore                            ### Files and directories to ignore from git history
├── data.json                             ### Data used in algorithmic design
├── data.txt                              ### data.json data provided in human readable format
├── index.html                            ### html to show SVG in browser
├── main.js                               ### Javascript that takes i) data.json as data, ii) style.css styling, and iii) d3 library for visualization to create SVG
├── package-lock.json                     ### [describes the exact tree that was generated after npm i](https://docs.npmjs.com/files/package-lock.json/)
├── package.json                          ### [project metadata](https://docs.npmjs.com/cli/v8/configuring-npm/package-json) (replace description and author)
└── style.css                             ### CSS styles for visualization
```
