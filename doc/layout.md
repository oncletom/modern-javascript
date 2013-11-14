# Repository Layout

This repository layout is suitable for *frontend projects*, *backend projects* and any other kind of applications such as *command line programs* and *Web based mobile applications*.

```
.
├── bin
├── config
├── dist
├── doc
├── i18n
├── lib
├── src
│   ├── assets
│   ├── controllers
│   ├── models
│   ├── partials
│   └── views
└── test
    ├── fixtures
    ├── functional
    └── unit
```

## Project Root

The project root contains the *essential files* of the project, which means:

- a `README` to provide context, example and enough details to get our hands on the project without reading a massive documentation
- packaging descriptors
- entry points/main files

```bash
LICENSE
README.md
package.json
```

## `/bin`

This folder contains **executable files**. Every file is assumed to be a system executable.

```bash
deploy.bat
deploy.sh
server.js
```

## `/config`

This folder contains **configuration files** such as database credentials, environment related values, default values etc.

Make sure no sensible information is committed in the wild, or appears in your versioning history.

```bash
database.yml
development.json
production.json
staging.json
```

## `/dist`

This folder contains **processed files for production use**. They are typically outputted by processing tasks and are usually not versioned.

*Notice*: some package systems (like [`bower`](http://bower.io/)) requires those files to be available in the versioning system. This is a workaround to avoid people installing the module to run the processing on their own.

```bash
index.html
main.min.js
```

## `/doc`

This folder contains the project **documentation files**.

They are usually written in a text format (like [Markdown](http://daringfireball.net/projects/markdown/) or [reStructuredText](http://docutils.sourceforge.net/rst.html)).

## `/i18n`

This folder contains **translation files**.

They might be organised as a per-locale folder basis to keep things organised.

## `/lib`

This folder contains the project **libraries and reusable components**.

## `/src`

This folder contains the **project source files**.

This is where lies the business logic of your application, and where you glue the different vendors and libraries.

### `/src/assets`

This folder contains **static assets**, **stylesheets** and any **user-facing files**.

### `/src/controllers`

This folder contains **route specific business logic files**.

Those files usually act as a glue between libraries and the view.

### `/src/models`

This folder contains **data models files**.

They are used by ORM, framework or database connection libraries.

### `/src/partials`

This folder contains **HTML fragments**.

These are mostly reusable document parts. They can be plain HTML, templating files (such as [Handlebars](http://handlebarsjs.com/) or [Swig](http://paularmstrong.github.io/swig/)).

### `/src/views`

This folder contains **HTML views**.

They can be plain HTML, templating files (such as [Handlebars](http://handlebarsjs.com/) or [Swig](http://paularmstrong.github.io/swig/)).

## `/test`

This folder contains **test files**, either they are unit tests, functional tests, headless browser tests or fixtures.
