# Diceware

A simple Diceware implementation in Clojure.

## Requirements

- Java 8
- [http://leiningen.org](leiningen)

## Build

1. `lein uberjar`

## Usage

Generate a passphrase of <n> Diceware words

    $ java -jar target/uberjar/diceware-0.1.0-SNAPSHOT/standalone.jar <num-words>

## Might be Useful

I place the following shell script in `$HOME/bin/diceware`:

    #!/bin/sh
    if [[ $# -lt 1 ]]; then
      echo "Generates, prints, and copies a passphrase to the clipboard"
      echo "usage: $(basename $0) <num-words>"
      exit 0
    fi

    java -jar $(dirname $0)/diceware-0.1.0-SNAPSHOT-standalone.jar $1 | tee /dev/tty | pbcopy


## License

Copyright © 2015 Christian Romney
Copyright © 2016 Hendrick Automotive Group

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
