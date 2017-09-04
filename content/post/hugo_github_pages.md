---
title: "Hugoを使ってGihub Pagesにブログを作成する手順"
date: 2017-08-23T09:37:05+09:00
draft: false
tags: [hugo,github pages]
---

## 参考URL

* 基本的に下記のURLの通り
	* (https://gohugo.io/hosting-and-deployment/hosting-on-github/#host-github-user-or-organization-pages)
	* (https://gohugo.io/getting-started/quick-start/)

## リポジトリを作成

* 表示用とコンテンツ用の2つを作成
	* &lt;username&gt;.github.io リポジトリ
	* コンテンツ用のディレクトリ
		* i.e. blog
		* README.mdは生成しなかった

## サイトを生成

* &lt;username&gt;.github.ioという名前でサイトをせいせい
```bash
hugo new site <username>.github.io
```


* Gitリポジトリとして初期化
```bash
git init
```


* コンテンツ用リポジトリをリモートに追加
```bash
git remote add origin https://github.com/<username>/blog
```


* &lt;username&gt;.github.io を public ディレクトリのsubmoduleとする
```bash
git submodule add -b master git@github.com:<USERNAME>/<USERNAME>.github.io.git public
```


* 参考URLのdeploy.shを作成

## テーマの登録

* cloneしている記事が多いがQuick Startではsubmoduleとしているのでそのようにする
```bash
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
```


* 後はQuick Startのように記事を追加したりすればOK
