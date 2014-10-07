# npmw

[![NPM](https://nodei.co/npm/npmw.png?compact=true)](https://nodei.co/npm/npmw/)

## Motivation

If you're like me and are not a big fan of having global modules installed on your system as a requirement to get up and running with any given project, then you might find this module handy.

This is nothing more than a wrapper (called `npmw`) installed on your project root. All it does is to spawn any given command line tool with the `node_modules/.bin` directory as part of the `$PATH`.

For example, if your project requires `gulp`, or `grunt` to be installed globally (`-g`), you can drop that requirement, and have them as simple `devDependencies` on your `package.json` and run them as follows:

* `./npmw gulp myTask`
* `./npmw grunt myTask`

Another example is `ionic`, which also requires `cordova` as a global module. Using `npmw` you can simply:

* `./npmw ionic serve`
* `./npmw ionic platform list`
* …

And your project is pretty munch self-contained! Win!

### What about `npm exec`?
Well, as of the time of this write up, `npm exec` does not currently support passing arguments. You should just use that once it does.

## Installation

```
npm install npmw --save-dev
```

## License
This is licensed under the feel-free-to-do-whatever-you-want-to-do license – [http://unlicense.org](http://unlicense.org)