# git-filettype

git-filettypeというGitのサブコマンドです。拡張子ごとの行数・ファイル数が取得できます。

## インストール

```
pip install git+https://github.com/akngw/git-filetype
```

## 使い方

```
usage: git-filettype [-h] [-c] [-I] [-i] [tree]

positional arguments:
  tree

optional arguments:
  -h, --help         show this help message and exit
  -c, --count        show the numbers of files and lines
  -I                 ignore binary files
  -i, --ignore-case  ignore case the extensions
```

git-ftという短い名前でも使えます。

## 使用例

```
$ git filetype -c
:2:150
.cfg:1:11
.md:1:1
.py:1:104
.toml:1:3
$
```
上記例の「:2:150」は、拡張子が無い場合です。

treeを省略するとHEADです。

ファイルおよびバイナリファイルかどうかの認識は、「git grep -c ''」「git grep -Ic ''」の結果に依存しています。
