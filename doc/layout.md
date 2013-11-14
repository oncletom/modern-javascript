# Repository Layout


```
.
├── bin
├── config
├── dist
├── doc
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
$ ls -l . | grep ^- | awk '{print $9}'
LICENSE
README.md
package.json
```

## `/bin`

This folder contains **executable files**. Every file is assumed to be a system executable.

```bash
$ ls -l ./bin | grep ^- | awk '{print $9}'
deploy.bat
deploy.sh
server.js
```

## `/config`

This folder contains **configuration files** such as database credentials, environment related values, default values etc.

Make sure no sensible information is committed in the wild, or appears in your versioning history.

```bash
$ ls -l ./config | grep ^- | awk '{print $9}'
database.yml
development.json
production.json
staging.json
```

## `/dist`

This folder contains **processed files for production use**. They are typically outputted by processing tasks and are usually not versioned.

*Notice*: some package systems (like [`bower`](http://bower.io/)) requires those files to be available in the versioning system. This is a workaround to avoid people installing the module to run the processing on their own.

```bash
$ ls -l ./dist | grep ^- | awk '{print $9}'
index.html
main.min.js
```

## `/doc`

This folder contains the project **documentation files**.

They are usually written in a text format (like [Markdown](http://daringfireball.net/projects/markdown/) or [reStructuredText](http://docutils.sourceforge.net/rst.html)).

## `/lib`

This folder contains the project **libraries and reusable components**.

## `/src`

This folder contains the **project source files**.

This is where lies the business logic of your application, and where you glue the different vendors and libraries.

## `/test`

This folder contains **test files**, either they are unit tests, functional tests, headless browser tests or fixtures.
