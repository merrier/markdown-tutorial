# shellhub

[![NPM version](https://img.shields.io/npm/v/shellhub.svg?style=flat)](https://www.npmjs.org/package/shellhub)
[![Build Status](https://travis-ci.org/harttle/shellhub.svg?branch=master)](https://travis-ci.org/harttle/shellhub)
[![Coverage Status](https://img.shields.io/coveralls/harttle/shellhub/master.svg)](https://coveralls.io/github/harttle/shellhub?branch=master)
[![Dependency manager](https://david-dm.org/harttle/shellhub/status.svg)](https://david-dm.org/harttle/shellhub)

An HTTP server to provide streaming ports for shell scripts, typically used for git hooks.

## Installation

```
npm install -g shellhub
```

## Usage

Make a `shellhubrc.json` in current directory:

```json
{
    "host": "0.0.0.0",
    "port": 8888,
    "stack": true,
    "scripts": {
        "/hello/world": {
            "cwd": "/Users/harttle/src/shellhub/demo/",
            "cmd": "hello-world.sh"
        }
    }
}
```

Run `shellhub` with default `shellhubrc.json` in current directory:

```bash
$ shellhub
```

Open `http://localhost:8888/hello/world` in your favorite browser, or:

```bash
curl http://localhost:8888/hello/world
```

The output of `hello-world.sh` will be streamed to stdout.

## Options

Name | Default | Description
--- | --- | ---
`host` | `"localhost"` | The host to bind with
`port` | `8080` | The port to bind with
`stack` | `true` | Whether or not print stack when there's an error
`scripts` | `{}` | Map from pathname to shell entry, the pathname can be arbitrary string
`scripts.cwd` | `undefined` | The work directory for the shell command, resolve based on the config file
`scripts.cmd` | `undefined` | The shell command to run, which will be passed to `bash -c`

## Q&A

### Can I use a config other than `./shellhubrc.json`?

```bash
$ shellhub -c path/to/your/shellhubrc.json
```

### Where can I find the logs?

Logs are printed to STDOUT, with datetime and traceID:

```
[2016-11-20T14:39:25.475Z][002] PATH: /hello/world
[2016-11-20T14:39:25.475Z][002] CWD: /Users/harttle/src/shellhub/demo/
[2016-11-20T14:39:25.475Z][002] CMD: bash hello-world.sh
[2016-11-20T14:39:25.495Z][002]
[2016-11-20T14:39:25.495Z][002] STDOUT:
[2016-11-20T14:39:25.495Z][002] Hello, World!
[2016-11-20T14:39:25.495Z][002] Hi, Hell!
```

### How to run this in background?

It's recommended to introduce a process manager like [pm2][pm2].

[pm2]: https://github.com/Unitech/pm2
