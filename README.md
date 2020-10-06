The project is generated with `npx -p @angular/cli ng new sample --minimal`.

Repro steps:

```
$ git clone ...
$ git checkout before
$ yarn
$ yarn run ng build
$ tree -d -L 5 > tree_before.txt
$ yarn add @ng-bootstrap/ng-bootstrap
$ tree -d -L 5 > tree_after.txt
$ git diff --no-index tree_before.txt tree_after.txt
```
