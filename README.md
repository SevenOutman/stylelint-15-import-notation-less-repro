# Stylelint 15 `import-notation` false positive in Less reproduction

This repo is a reproduction of a false positive in Stylelint 15's `import-notation` rule when used with Less ([related issue](https://github.com/stylelint/stylelint/issues/7096)).

There're 2 Less files in this repo:

- `a.less` which contains some random styles
- `b.less` which imports `a.less` with `@import` at-rule

## Steps to reproduce

1. Clone this repo and install Stylelint with `pnpm i`
2. Run `pnpm lint` to see the unexpected output

```
pnpm lint

> stylelint *.less


b.less
 1:9  ✖  Expected ""a"" to be "url("a")"  import-notation

1 problem (1 error, 0 warnings)

```
