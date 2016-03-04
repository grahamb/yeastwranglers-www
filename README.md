# Yeast Wranglers

> Yeast Wranglers www

## To get started

```sh
$ gulp [--prod]
```

And you'll have a new Jekyll site generated for you and displayed in your
browser. Neato. If you want to run it with production settings, just add
`--prod`.

## Usage

```sh
$ gulp build [--prod]
```

```sh
$ gulp deploy
```

## Github
For more information on how to use your new project, please refer to the [README
on Github](https://github.com/sondr3/generator-jekyllized).

## Owner

> [chrisvdp]()

## for SSL issue

If you get `SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed`

`wget http://curl.haxx.se/ca/cacert.pem`
`SSL_CERT_FILE=cacert.pem gulp`
