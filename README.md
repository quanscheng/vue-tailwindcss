# vue-tailwindcss

## init

1. tailwindcss

```shell
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

2. tailwind.config.js

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./index.html', './src/**/*.{vue,js,ts,jsx,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. /src/assets 中创建`tailwind.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

4. `/src/assets/main.css`导入

```css
@import './tailwind.css'; /* 放在顶部 */
```

## optional

5. 单独定义 CSS 属性

```shell
npm install -D postcss-import
```

在实用类中使用 @apply:

```js
<style lang="scss">
.about {
  @apply lg:min-h-screen lg:flex lg:items-center;
  h1 {
    @apply text-xl font-medium text-white;
  }
}
</style>
```

6. 添加 SVG loader (SVG 作为组件导入)

```shell
npm install vite-svg-loader --save-dev
```

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
