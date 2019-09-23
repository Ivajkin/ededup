# ededup
Easy to use copy/paste detector for programming source code. https://github.com/Ivajkin/ededup

# Usage

One way to use it as global package through

```ededup --path SOMEPATH_TO_ANALYSE```

command.

Other way is through local package in devDependencies:

Add to package.json scripts:

```"dedup": "(npm list -g ededup || npm i -g ededup) && (ededup --path SOMEPATH_TO_ANALYSE)",```

or just install once globally ```npm i -g ededup``` and add ```"dedup": "ededup --path SOMEPATH_TO_ANALYSE",``` to package.json scripts

or add to package.json scripts:

```"dedup-local": "sh ./node_modules/ededup/bin/ededup --path SOMEPATH_TO_ANALYSE",```

and add ```"ededup": "^1.0.7"``` devDependency then.

# How to

## Install 

```npm i -g ededup```

## Use

```ededup --path SOMEPATH_TO_ANALYSE```

# Notes

```npm list -g ededup || npm i -g ededup``` is to install in case it is not installed yet. Not updates ededup even if never version available.

License is in LICENSE file. 

## Known issues
[ededup-issue-001] you should probably add ".jscpd" to .gitignore file when you use dedup

# Plans

## Todo

1. fix [ededup-issue-001] by changing arguments supplied or something like that
2. Autoadd to scan ignore paths from current directory's .gitignore file
3. Sort output by priorities (by lines of code duplicated)