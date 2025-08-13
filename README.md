# 石射のブログ

ここは，石射のブログを格納したリポジトリです．
完成品は Note とか自分の web ページとかで公開します．
このリポジトリは，そのブログの内容のみを配置したものです．
View と Model は分けるべきというノリで分離しました．

公開する web ページのリポジトリでは，このリポジトリを submodule などで参照することを想定しています．

## 構成

Markdown + Pandoc

- 基本的には Markdown
- 引用に BibTex を使うために Pandoc

## 記事のコンパイル

以下のコマンドを実行すればいい  
`pandoc "path_to_input.md" -o "path_to_output.md" --citeproc --to commonmark`

例：  
`pandoc ".\blogs\ボイスチェンジャーを利用するための音声経路の整備\main.md" -o ".\blogs\ボイスチェンジャーを利用するための音声経路の整備\output.md" --citeproc --to commonmark`
