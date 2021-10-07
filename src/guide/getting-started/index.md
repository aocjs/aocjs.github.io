# Getting started

:::warning
This guide is temporary. Before [@aocjs/cli](https://github.com/aocjs/cli) v1 is released, an automatic method will be availible making easier first steps.
:::


## Instalation

To get started you need to install ***@aocjs/cli***.

```sh
npm i @aocjs/cli
```


## Configuration

Before start running your code, you need to specify your **session cookie** by creating a [config file](/config/) named `.aocrc`. After that, copy your cookie from ***adventofcode.com***. If you don't know how, follow [this steps](/guide/data/#how-to-retrieve-your-cookie).

```json
{
  "$schema": "https://raw.githubusercontent.com/aocjs/cli/main/schema/schema.json",
  "session": "YOUR PRIVATE KEY"
}
```


## TypeScript

If you want to use TypeScript to solve your problems, you must specify it in your [config file](/config/) by setting a ***compiler***.

```json
{
  "$schema": "https://raw.githubusercontent.com/aocjs/cli/main/schema/schema.json",
  "session": "YOUR PRIVATE KEY",
  "compiler": "ts"
}
```

You will need **ts-node** too.

```sh
npm i ts-node
```


## 🚀 Start up

Now you can start your first day by running the following command. This will create and run `day1.js` or `day1.ts`, including required file structure.

```sh
npx aoc start day1
```

You can simplify your run command, by adding the next script to your `package.json`.

```json
"scripts": {
  "start": "npx aoc start"
},
```

If you do so, you could run day1 as follows.

```sh
npm start day1
```
