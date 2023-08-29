---
title: "Node.jsのプロジェクト管理"
emoji: "🗂"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: []
published: True
---

# はじめに　
Node.jp(npm)を使ったプロジェクトの管理方法についてまとめる

# npmとは
* Node.jsのパッケージマネージャ
* package.jsonというファイルに設定を書いて使用

pythonに置き換えると  
* npm = pip
* package.json = requirement.txt

# Node.jsプロジェクトのディレクトリ構造
* プロジェクト  
特定のワーキングディレクトリ上にフォルダーを作成  
（例：hr-toyotaやudemy-aws-lambdaのこと）  
![](/images/npm_tree_list.png)

* プロジェクト内でパッケージをインストールする
```
$mkdir hr-toyota         #プロジェクトとなるフォルダーを作成  
$cd hr-toyota  
$npm init                #package.jsonを作成
$npm install --global serverless@3.24.1  
　#serverless framewarkをグローバルインストール
$npm list -g             #グローバルインストールされたパッケージをリスト
/home/ec2-user/.nvm/versions/node/v16.20.1/lib #Cloud9環境の場合はココへ
├── cdk@2.87.0
├── coffeescript@2.7.0
├── corepack@0.17.0
├── esformatter@0.11.3
├── js-beautify@1.14.8
├── npm@8.19.4
├── prettier@3.0.0
├── serverless@3.24.1
└── typescript@3.7.5
$ls -l /home/ec2-user/.nvm/versions/node/v16.20.1/lib/node_modules
 #当パスのnode_modulesへパッケージがインストールされる
 #ローカルインストールの場合は、カレントディレクトリのnode_modulesへインストールされる。
 #ローカルインストールしたい場合は、[--save]オプションをつける。
total 0
drwxr-xr-x 11 ec2-user ec2-user 154 Jul 21 07:23 .
drwxr-xr-x  3 ec2-user ec2-user  26 Jun 20 14:17 ..
drwxrwxr-x  4 ec2-user ec2-user 103 Jul 14 15:11 cdk
drwxrwxr-x  4 ec2-user ec2-user 114 Jul 14 14:57 coffeescript
drwxr-xr-x  4 ec2-user ec2-user 106 Jun 20 14:17 corepack
drwxrwxr-x  6 ec2-user ec2-user 134 Jul 14 15:11 esformatter
drwxrwxr-x  4 ec2-user ec2-user  88 Jul 14 15:11 js-beautify
drwxr-xr-x  7 ec2-user ec2-user 153 Jun 20 14:17 npm
drwxrwxr-x  5 ec2-user ec2-user 263 Jul 14 15:11 prettier
drwxrwxr-x  8 ec2-user ec2-user 187 Jul 21 07:23 serverless
drwxrwxr-x  5 ec2-user ec2-user 198 Jul 14 14:57 typescript
```

