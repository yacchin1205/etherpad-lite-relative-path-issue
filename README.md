# etherpad-lite-relative-path-issue

This repository is a demonstration of the issue https://github.com/ether/etherpad-lite/issues/6620 with etherpad-lite's relative path handling.

## Pre-requisites

- Docker Engine

## Steps to reproduce

1. Clone this repository
2. Run `docker compose up`
3. Visit `http://localhost:9002/sub/path/etherpad/p/foobar`
4. You will see the following error:

```
foobar:681
 GET http://localhost:9002/sub/path/padbootstrap-AWbfvdxaiSQ.min.js net::ERR_ABORTED 404 (Not Found)
```

## Expected behavior

The etherpad-lite page should load the padbootstrap-XXXXXXXX.min.js file from the correct path like `http://localhost:9002/sub/path/etherpad/padbootstrap-AWbfvdxaiSQ.min.js`.
