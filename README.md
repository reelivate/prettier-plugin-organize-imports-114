# Prettier slowness repo

https://github.com/simonhaenisch/prettier-plugin-organize-imports/issues/114

## Steps to reproduce

1. Clone this repo
2. Run `npm install`
3. Run `composer install` (composer is PHP's package manager)
4. Run `npm run fmt`

Here's the result I get:

```
npm run fmt

> fmt
> npx prettier --write "resources/**/*.{js,jsx,vue,css,pcss,scss}"

resources/js/TableComponent.vue 1297ms (unchanged)
resources/js/TableComponent2.vue 620ms (unchanged)
resources/js/Test.vue 369ms (unchanged)
resources/js/Test2.vue 357ms (unchanged)
```

Oddly, the amount of time it takes to format seems to be related to the number of files in `vendor/` even though that directory is ignored by prettier.