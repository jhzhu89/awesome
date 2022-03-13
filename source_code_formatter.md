# Source Code Formatter

## Bash

### [shfmt](https://github.com/mvdan/sh)

Example:
```bash
shfmt -l -w script.sh
```

## JSON

### jq

```bash
#!/bin/bash -xe
echo $PWD

for dent in `ls *.json`
do
  if [ -f $dent ];
  then
    echo "formatting $dent..."
    jq . $dent > $dent.tmp && mv $dent.tmp $dent
  fi
done
```

## Javascript

### jsbeautifier

```bash
 pip install jsbeautifier
```

```bash
js-beautify -j -s 2 -E --space-after-named-function -r -b collapse *.js
```