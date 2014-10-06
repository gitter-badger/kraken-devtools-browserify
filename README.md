kraken-devtools-browserify
==========================
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/eBay-European-Product-Development/kraken-devtools-browserify?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Browserify plugin for kraken-devtools


## Usage

Add:

```json
"browserify": {
    "module": "kraken-devtools-browserify",
    "files": "/js/**/*.js"
}
```

to your kraken development configuration (config/development.json) under middleware.devtools.module[name=kraken-devtools].arguments.

Should look like this:

<pre>
"middleware": {
    ...

    "devtools": {
        ...

        "module": {
            "name": "kraken-devtools",
            "arguments": [
                ...
                {
                    ...
                    "css": {
                        "module": "kraken-devtools/plugins/less",
                        "files": "/css/**/*.css"
                    },
<b>
                    "browserify": {
                        "module": "kraken-devtools-browserify",
                        "files": "/js/**/*.js"
                    },
</b>
                    "copier": {
                        "module": "kraken-devtools/plugins/copier",
                        "files": "**/*"
                    }
                }
            ]
        }
    }
}
</pre>