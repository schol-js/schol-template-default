# schol-template-default

> Default template for [schol](https://github.com/schol-js/schol).

## Demo

[![thumbnail](https://github.com/schol-js/schol-template-default/blob/master/media/example.png)](https://schol-js.github.io/schol-template-default)

## Usage

Use this schol template to get started writing a research paper. You can also use this template a starting point for developing new templates.

### Create a new schol project

To create a new project using this template, create a new folder for the project, navigate into it, and initialize a new schol project with `schol init`:

```sh
mkdir assignment
cd assignment
schol init --template schol-template-default
```

`--template` is optional in this case because it is the default for new schol projects.

### Create a new template

To use this template as a starting point for a new template, fork, clone, or copy this repo, and hack away!

You can then either publish your template on npm, or simply use it locally.

A few things to keep in mind:

 - Make sure your package name starts with `schol-template-` to make it easy to find

 - The `main` property in `package.json` must point to a valid [EJS](http://ejs.co/) template located in the root of the `src/` directory.

 - Anything placed in `src/` will be copied to the `src/` folder of any schol project initialized with the template.

 - Documents within `src/` will be processed as EJS templates when initialized by `schol init`. The current `date` will always be provided to these templates in YYYY-MM-DD format.

 - Test and develop your template by running the following from within your template directory:

   ```sh
   npm link
   npm link schol-template-default // Or whatever your template is
   schol edit -p
   ```
  
   This will use the current directory (your template directory) as the template, and will run your  `src/` files through EJS to inject the date before further processing.

 - Include example output of your template in the `docs` folder with `schol render -p` and [set up your GitHub repository to publish from the `docs/` folder in your template project.](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#publishing-your-github-pages-site-from-a-docs-folder-on-your-master-branch). This will allow users to see what your template looks like before they use it.

 - Include a screenshot of your template output in `media/example.png`. Use a square aspect ratio with a resolution of at least 898x898.

 - Once published to npm and GitHub, add your template to the [schol templates list](https://github.com/schol-js/schol/wiki/templates)!

## Credits

 - Github Flavored Markdown styling adapted from Sindre Sorhus: https://github.com/sindresorhus/github-markdown-css
 - Bibliography styles adapted from Zotero: https://github.com/zotero/zotero/blob/4aaec5f091530a9e377ac0f05c5e2beb2da995d1/chrome/content/zotero/xpcom/cite.js