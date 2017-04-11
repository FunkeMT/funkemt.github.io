---
title: shell
category: Snippets
---

### shebang

```sh
#!/bin/bash
```

### stdout to var

```sh
# whole output
var="$(ls -al)"

# last line
var="$(ls -al | tail -1)"
```

### Script parameters

* `$*` Returns a single string (``$1, $2 ... $n'')
* `$1, $2 ... $n` Refers to a numbered argument to the script
* `$0` Refers to the name of the script itself
* `$#` Refers to the number of arguments
* Check if arguments are available

    ```sh
    if [ $# -eq 0 ]
      then
        echo "No arguments supplied"
    fi
    ```
* Switch Case

    ```sh
    case "$1" in
      "foo")
        doFoo
        ;;
      "bar")
        doBar
        ;;
      *)
        echo "You have failed to specify what to do correctly."
        exit 1
        ;;
    esac
    ```