cli-demo
=================

A new CLI generated with oclif


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/cli-demo.svg)](https://npmjs.org/package/cli-demo)
[![Downloads/week](https://img.shields.io/npm/dw/cli-demo.svg)](https://npmjs.org/package/cli-demo)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g cli-demo
$ XTM COMMAND
running command...
$ XTM (--version)
cli-demo/0.0.0 darwin-arm64 node-v18.19.0
$ XTM --help [COMMAND]
USAGE
  $ XTM COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`XTM hello PERSON`](#xtm-hello-person)
* [`XTM hello world`](#xtm-hello-world)
* [`XTM help [COMMAND]`](#xtm-help-command)
* [`XTM plugins`](#xtm-plugins)
* [`XTM plugins add PLUGIN`](#xtm-plugins-add-plugin)
* [`XTM plugins:inspect PLUGIN...`](#xtm-pluginsinspect-plugin)
* [`XTM plugins install PLUGIN`](#xtm-plugins-install-plugin)
* [`XTM plugins link PATH`](#xtm-plugins-link-path)
* [`XTM plugins remove [PLUGIN]`](#xtm-plugins-remove-plugin)
* [`XTM plugins reset`](#xtm-plugins-reset)
* [`XTM plugins uninstall [PLUGIN]`](#xtm-plugins-uninstall-plugin)
* [`XTM plugins unlink [PLUGIN]`](#xtm-plugins-unlink-plugin)
* [`XTM plugins update`](#xtm-plugins-update)

## `XTM hello PERSON`

Say hello

```
USAGE
  $ XTM hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ XTM hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/oclif-demo/xtm-cli/blob/v0.0.0/src/commands/hello/index.ts)_

## `XTM hello world`

Say hello world

```
USAGE
  $ XTM hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ XTM hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/oclif-demo/xtm-cli/blob/v0.0.0/src/commands/hello/world.ts)_

## `XTM help [COMMAND]`

Display help for XTM.

```
USAGE
  $ XTM help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for XTM.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.0.21/src/commands/help.ts)_

## `XTM plugins`

List installed plugins.

```
USAGE
  $ XTM plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ XTM plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/index.ts)_

## `XTM plugins add PLUGIN`

Installs a plugin into XTM.

```
USAGE
  $ XTM plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into XTM.

  Uses bundled npm executable to install plugins into /Users/pengrongshu/.local/share/XTM

  Installation of a user-installed plugin will override a core plugin.

  Use the XTM_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the XTM_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ XTM plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ XTM plugins add myplugin

  Install a plugin from a github url.

    $ XTM plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ XTM plugins add someuser/someplugin
```

## `XTM plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ XTM plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ XTM plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/inspect.ts)_

## `XTM plugins install PLUGIN`

Installs a plugin into XTM.

```
USAGE
  $ XTM plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into XTM.

  Uses bundled npm executable to install plugins into /Users/pengrongshu/.local/share/XTM

  Installation of a user-installed plugin will override a core plugin.

  Use the XTM_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the XTM_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ XTM plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ XTM plugins install myplugin

  Install a plugin from a github url.

    $ XTM plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ XTM plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/install.ts)_

## `XTM plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ XTM plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ XTM plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/link.ts)_

## `XTM plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ XTM plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ XTM plugins unlink
  $ XTM plugins remove

EXAMPLES
  $ XTM plugins remove myplugin
```

## `XTM plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ XTM plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/reset.ts)_

## `XTM plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ XTM plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ XTM plugins unlink
  $ XTM plugins remove

EXAMPLES
  $ XTM plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/uninstall.ts)_

## `XTM plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ XTM plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ XTM plugins unlink
  $ XTM plugins remove

EXAMPLES
  $ XTM plugins unlink myplugin
```

## `XTM plugins update`

Update installed plugins.

```
USAGE
  $ XTM plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.0.19/src/commands/plugins/update.ts)_
<!-- commandsstop -->
