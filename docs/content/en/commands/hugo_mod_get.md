---
title: "hugo mod get"
slug: hugo_mod_get
url: /commands/hugo_mod_get/
---
## hugo mod get

Resolves dependencies in your current Hugo project

### Synopsis


Resolves dependencies in your current Hugo project.

Some examples:

Install the latest version possible for a given module:

    hugo mod get github.com/gohugoio/testshortcodes

Install a specific version:

    hugo mod get github.com/gohugoio/testshortcodes@v0.3.0

Install the latest versions of all direct module dependencies:

    hugo mod get
    hugo mod get ./... (recursive)

Install the latest versions of all module dependencies (direct and indirect):

    hugo mod get -u
    hugo mod get -u ./... (recursive)

Run "go help get" for more information. All flags available for "go get" is also relevant here.

Note that Hugo will always start out by resolving the components defined in the site
configuration, provided by a _vendor directory (if no --ignoreVendorPaths flag provided),
Go Modules, or a folder inside the themes directory, in that order.

See https://gohugo.io/hugo-modules/ for more information.



```
hugo mod get [flags] [args]
```

### Options

```
  -h, --help   help for get
```

### Options inherited from parent commands

```
      --clock string               set the clock used by Hugo, e.g. --clock 2021-11-06T22:30:00.00+09:00
      --config string              config file (default is hugo.yaml|json|toml)
      --configDir string           config dir (default "config")
  -d, --destination string         filesystem path to write files to
  -e, --environment string         build environment
      --ignoreVendorPaths string   ignores any _vendor for module paths matching the given Glob pattern
      --logLevel string            log level (debug|info|warn|error)
      --noBuildLock                don't create .hugo_build.lock file
      --quiet                      build in quiet mode
  -M, --renderToMemory             render to memory (mostly useful when running the server)
  -s, --source string              filesystem path to read files relative from
      --themesDir string           filesystem path to themes directory
```

### SEE ALSO

* [hugo mod](/commands/hugo_mod/)	 - Manage modules

