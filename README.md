## Archival Notice

📁🗄📜**Repository Archived**

This repository has been archived and will no longer be maintained by Heroku.

**What this means:**
- Pull requests and issue tracking have been disabled.
- The project will not receive updates and no new features or security updates will be released.
- The repository is now read-only.
- The plugin will still be available to use but may be deprecated.

**Why was it archived?**
This project is considered complete and active development has concluded.

**What if I need to make a change?**
If you wish to continue development, please consider forking the repository and maintaining your own version.

cli-flags
=========

[![CircleCI](https://circleci.com/gh/heroku/cli-flags/tree/master.svg?style=svg)](https://circleci.com/gh/heroku/cli-flags/tree/master)

CLI flag parser.

Usage:

```js
const CLI = require('cli-flags')

const {flags, args} = CLI.parse({
  flags: {
    'output-file': CLI.flags.string({char: 'o'}),
    force: CLI.flags.boolean({char: 'f'})
  },
  args: [
    {name: 'input', required: true}
  ]
})

if (flags.force) {
  console.log('--force was set')
}

if (flags['output-file']) {
  console.log(`output file is: ${flags['output-file']}`)
}

console.log(`input arg: ${args.input}`)

// $ node example.js -f myinput --output-file=myexample.txt
// --force was set
// output file is: myexample.txt
// input arg: myinput
```
