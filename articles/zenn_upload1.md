---
title: "ローカルで作成したMDファイルをZennへアップロードする"
date: 2023-08-14
type: "tech"
topics: []
published: true
---


ローカルで作成したMDファイルをZennへアップロードする

ZennへアップロードするMarkdownファイルに画像を埋め込む場合相対パスはNG
必ず絶対パスで指定が必要。vscode上なら画像埋め込みできる。
例
    OK  ![](/images/aaa.png)
    NG  ![](../images/aaa.png)