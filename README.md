# Steps

1. `yarn install --immutable`
2. `yarn nx run --verbose --parallel=1 --batch @nx-js-ts-problem/parent:build`


Console output:
```
yarn run v1.22.18
$ /home/oem/PhpstormProjects/nx-js-tsc-problem/node_modules/.bin/nx run --verbose --parallel=1 --batch @nx-js-ts-problem/parent:build

 NX   Running target build for project @nx-js-ts-problem/parent and 2 tasks it depends on:

———————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————

> nx run @nx-js-ts-problem/child:build

Compiling TypeScript files for project "@nx-js-ts-problem/child"...
Done compiling TypeScript files for project "@nx-js-ts-problem/child".

> nx run @nx-js-ts-problem/parent:pre-build

@nx-js-ts-problem/parent: > echo 'pre-build-parent'
@nx-js-ts-problem/parent: pre-build-parent

> nx run @nx-js-ts-problem/parent:build

Cannot read properties of null (reading 'tsConfig')

———————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————

 NX   Running target build for project @nx-js-ts-problem/parent and 2 tasks it depends on failed

Failed tasks:

- @nx-js-ts-problem/parent:build

Hint: run the command with --verbose for more details.

error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```
