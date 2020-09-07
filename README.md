
# node10

Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.  See [documentation](https://nodejs.org/en/)

## Maintainers

* The Core Planners: <chef-core-planners@chef.io>

## Type of Package

Binary package

### Use as Dependency

Binary packages can be set as runtime or build time dependencies. See [Defining your dependencies](https://www.habitat.sh/docs/developing-packages/developing-packages/#sts=Define%20Your%20Dependencies) for more information.

To add core/node10 as a dependency, you can add one of the following to your plan file.

##### Buildtime Dependency

> pkg_build_deps=(core/node10)

##### Runtime dependency

> pkg_deps=(core/node10)

### Use as Tool

#### Installation

To install this plan, you should run the following commands to first install, and then link the binaries this plan creates.

``hab pkg install core/node10 --binlink``

will add the following binaries to the PATH:

* /bin/node
* /bin/npm
* /bin/npx

For example:

```bash
$ hab pkg install core/node10 --binlink
» Installing core/node10
☁ Determining latest version of core/node10 in the 'stable' channel
```

#### Using an example binary

You can now use the binary as normal.  For example:

``/bin/node --help`` or ``node --help``

```bash
$ node --help
Usage: node [options] [ script.js ] [arguments]
       node inspect [options] [ script.js | host:port ] [arguments]

Options:
  -                                script read from stdin (default if no file name
                                   is provided, interactive mode if a tty)
  --                               indicate the end of node options
  --abort-on-uncaught-exception    aborting instead of exiting causes a core file
                                   to be generated for analysis
  -c, --check                      syntax check script without executing
...
...
```
