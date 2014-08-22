# Command Line Interface

## Usage

    Usage: duo [options] command|[file, ...] [out]

    Options:

      -h, --help             output usage information
      -V, --version          output the version number
      -c, --copy             opt to copy files instead of symlink
      -d, --development      include development dependencies.
      -g, --global <name>    expose entry as a global <name>
      -o, --output <dir>     set the output directory, defaulted to build/
      -q, --quiet            only print to stderr when there is an error
      -r, --root <dir>       root directory to build from.
      -t, --type <type>      set the entry type
      -u, --use <plugin>     use transform plugin
      -v, --verbose          show as much logs as possible
      -w, --watch            watch for changes and rebuild

## Examples

```bash
# build in.js to out.js
$ duo in.js > out.js

# build in.css to out.css
$ duo in.css > out.css

# build all files to duo.assets() (default: build/)
$ duo *.{js,css}

# watch all files and build to duo.assets()
$ duo watch *.{js,css}

# build all files to the out/ folder
$ duo *.{js,css} out

# watch all files and build to the out/ folder
$ duo watch *.{js,css} out

# build from stdin and output out.css
$ duo < in.css > out.css

# build using a plugin
$ npm install duo-whitespace
$ duo --use duo-whitespace in.styl > out.css
```

## Commands

    ls           list all dependencies.
    duplicates   show all duplicates.
