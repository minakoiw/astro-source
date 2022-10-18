# A Portfolio Website for Minako Williams

Basic website presence for Minako

*This website was built using [Astro JS](https://astro.build)*

## Adding and Editing Content on the Website

This website is designed to be easy to add and edit content.

### Changing Page Text

#### Landing Page

The quote on the landing page is simply a string in **src > pages > index.astro**. Simply replace the string.

#### About Page

The text for the About page can be as rich and long as you might want, so we've used a simple text file formatted for [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). The file is located at **src > mdContent > about-text.md**. Simply modify the file using the rules of Markdown and the about page is rewritten.

### Adding a Portfolio Piece

1. Take a picture of the artwork and resize it to around 800 pixels in width (preferably JPG). Add this file to the **public > assets > portfolio** folder with a good filename (title of the piece would be a good idea).
2. Add a file into the **src > mdPortolio** directory. The name of the file doesn't matter, though original files were named item1 .. item4. The filenames **must** end in **md**, though. All art pieces will show up in the portfolio page ordered from the most recent to the oldest.
3. The files must look like the following, where the items after the colons (**:**) must be replaced with the appropriate information for the artwork.
4. Currently, the description at the bottom of the file aren't used.
```
---
title: Artwork Title
date: September 15, 2022
imgUrl: "../assets/portfolio/<image filename>.jpg"
dimensions: 14 x 22 inches
materials: Paint, straws, strings, duct tape, and paint markers
---

(Descriptive details can go here, though these are not currently shown in the website.)

```
### Adding Exhibitions

To add an exhibition to the Exhibitions page, add a file to the **src > mdExhibitions** folder. Once again, they must have a filename ending in **.md** and they must be formatted as [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). 

The content at the bottom of the last set of hyphens (---) is shown on the page. In the examples given to me, only links were included, though complete descriptions, including headers, photos and descriptions can be included there (as Markdown).

```
---
title: BofA Juried Exhibition
locationName: The Atrium at PNCA
address1: 511 NW Broadway
city: Portland
state: "OR"
zip: "97209"
date: "2022-04-07"
---

[https://pncaevents.willamette.edu/events/397](https://pncaevents.willamette.edu/events/397)

```

## Required Tools

Astro requires the following tools to actually build the website

* [Git](https://git-scm.org) for source control
* [Node JS](https://nodejs.org) for the package management and JS engine
* Some kind of source code editor, like [Visual Studio Code](https://code.visualstudio.com/Download)

You'll need to know HTML, CSS, JavaScript and maybe some TypeScript to go wild on changing the hard stuff.

## Building this project

After installing the tools above execute the following commands in a terminal. Choose a directory to install your project in and call it **\<home>**

```
cd <home>
git clone https://github.com/minakoiw/astro-source portfolio
cd portfolio
npm install
```
At this point, you should be set up to run the development version on your computer.
```
npm run dev
```
Your computer should be running the website at this point. There should be a message on the terminal saying **Local http://127.0.0.1:3000** which can be translated to **localhost:3000**. Start a browser (like Chrome, Firefox, Edge or Safari) and type into the address bar **localhost:3000**. You should see the website in the browser.

As you make changes to your code or add or edit any of the text, you should see changes immediately appear on the website as soon as you save the files. Occasionally, you may need to stop and restart the development server (\<ctrl>-c will stop the server, the type in ```npm run dev``` to restart it).

When you're done making changes type ```npm run build``` at the terminal to build the static website files. The entire website will be in the **dist** folder.




## General Astro Commands 

All commands are run from the root of the project, from a terminal:

| Command                | Action                                           |
| :--------------------- | :----------------------------------------------- |
| `npm install`          | Installs dependencies                            |
| `npm run dev`          | Starts local dev server at `localhost:3000`      |
| `npm run build`        | Build your production site to `./dist/`          |
| `npm run preview`      | Preview your build locally, before deploying     |
| `npm run astro ...`    | Run CLI commands like `astro add`, `astro check` |
| `npm run astro --help` | Get help using the Astro CLI                     |

