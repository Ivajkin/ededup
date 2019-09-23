# ededup
Easy to use copy/paste detector for programming source code. https://github.com/Ivajkin/ededup

# Usage

One way to use it as global package through

```ededup --path SOMEPATH_TO_ANALYSE```

command.

Other way is through local package in devDependencies:

Add to package.json scripts

```"dedup": "(npm list -g ededup || npm i -g ededup) && (ededup --path SOMEPATH_TO_ANALYSE)",```

or add to package.json scripts

```"dedup-local": "./ededup/bin/ededup --path SOMEPATH_TO_ANALYSE",```

and add ```"ededup": "^1.0.7"``` devDependency then.