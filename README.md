[![Netlify Status](https://api.netlify.com/api/v1/badges/45817baa-d123-44d0-8b54-6aafaff30bf1/deploy-status)](https://app.netlify.com/sites/hopeful-meninsky-bf657b/deploys)
# Vue JS Crash Course - 2019

Brad Traversy

[![YouTube Video](notes/1-reusable-components.png)](https://youtu.be/Wy9q22isx3U)
[video link --^](https://youtu.be/Wy9q22isx3U)

![Max- the big picture](notes/vue-cli-the-big-picture.png)

## What you should know

### JavaScript Fundamentals

```md
- [X] Objects

- [X] Arrays

- [X] Conditionals
```

#### It may help to learn these first

```md
[/] ES6 Module Syntax

[/] High Order Array Methods
- [ ] forEach
- [ ] map
- [ ] filter

[/] Arrow Functions

[/] Fetch API & Promises
```

---

## Reusable Components

![Reusable Components](notes/1-reusable-components.png)

## Anatomy of a Component

![Anatomy of a Component](notes/2-component-anatomy.png)

## VUE-CLI 3

![vue cli 3](notes/3-vue-cli3.png)

### CLI Commands

#### Install vue globally

```bash
npm -g @vue/cli
```

#### Check version installed

```bash
vue --version
```

#### Create Project

```bash
vue create
 - select defaults (babel, etc)

cd test
npm run serve

```

#### Vue GUI (dashboard, analytics, etc.)

Start GUI

```bash
vue ui
```

Stop Server

```bash
^C  // ctrl+c
```

## Vuex for State Management (not covered)

![Vuex for State Management](notes/4-vuex-for-state-management.png)


## The Big Picture

![vue-cli-the-big-picture.png](vue-cli-the-big-picture.png)

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
