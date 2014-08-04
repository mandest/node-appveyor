# AppVeyor

A javascriptable CLI for AppVeyor for node projects. It is basically the
AppVeyor equivalent of [travisjs](https://www.npmjs.org/package/travisjs).

Install with `npm install appveyor -g`

```
Usage: appveyor <command>

command
  auth      set the auth token for AppVeyor
  hook      activate AppVeyor for the current project
  yml       create a appveyor.yml file in the current directory
  badge     print the text for the badge (shields.io)
```

The commands map to the specific functions. For now look at
the source code for details.
```js
var AppVeyor = require('appveyor')
var appveyor = new AppVeyor()
appveyor.auth('<your token>') // saved locally
appveyor.badge(process.stdout) // prints the badge
```