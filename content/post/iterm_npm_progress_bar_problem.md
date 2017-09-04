---
title: "iTerm2でnpm install,yarnコマンドで表示されるプログレスバーがおかしくなる問題の対処方法"
date: 2017-09-04T22:42:57+09:00
tags: [npm,yarn,item2]
draft: false
---

# プログレスバー自体を表示しない

* npm set progress=false
* yarn --no-progress

# iTerm2の設定を帰る

* Preferences -> Profiles -> Textタブ
	*	Treat ambiguous-width characters as double width (not recommended) のチェックをはずす
