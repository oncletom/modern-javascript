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

```bash
$ ls -l ./config | grep ^- | awk '{print $9}'
database.yml
development.json
production.json
staging.json
```

## `/dist`

```bash
$ ls -l ./dist | grep ^- | awk '{print $9}'
index.html
main.min.js
```

## `/doc`

This folder contains the project **documentation**.

## `/lib`

This folder contains the project **libraries and reusable components**.


## `/src`

This folder contains the **project source files**.

```bash
$ ls -1 ./src

```

## `/test`

This folder contains **test files**, either they are unit tests, functional tests, headless browser tests or fixtures.
