---
layout: post
title: Mac 常用资源
category: 资源
tags: Mac
keywords: Mac
description:
---

## 常用软件

### Alfred

#### Alfred常用Workflow

- [Dash](http://kapeli.com/dash)
- [Dict - Lookup Word](https://github.com/liberize/alfred-dict-workflow)
- [Reminders](http://www.alfredforum.com/topic/917-reminders/)
- [Evernote](http://support.alfredapp.com/evernote)
- [Notes](http://www.alfredforum.com/topic/1009-notes/)

## 常用命令

### 开启关闭dashboard

关闭

    defaults write com.apple.dashboard mcx-disabled -boolean YES
    killall Dock

开启

    defaults write com.apple.dashboard mcx-disabled -boolean NO
    killall Dock

### 剪贴板操作
写入剪切板

    echo 'test' > pbcopy
    cat testfile > pbcopy

读取剪贴板

    pbpaste > testfile
    pbpaste | cat

### 开启关闭Hidpi
开启

    sudo defaults write /Library/Preferences/com.apple.windowserver DisplayResolutionEnabled -bool YES

关闭

    sudo defaults delete /Library/Preferences/com.apple.windowserver DisplayResolutionDisabled
### Finder 标题栏显示完整路径

```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
```

### 修改Dock隐藏和出现时间

```bash
defaults write com.apple.dock autohide-delay -int 0
defaults write com.apple.dock autohide-time-modifier -float 0.4
killall Dock
```


### 设置iterm中option为alt(meta)键

![option-to-meta]()

### 删除dropbox冲突文件

    find . -type f -name "* conflicted *" -exec rm -f {} \;

### 清空Launchpad（删除掉）

    sqlite3 ~/Library/Application\ Support/Dock/*.db 'DELETE FROM apps;' && killall Dock

### 重置Launchpad

    rm -f ~/Library/Application\ Support/Dock/*.db && killall Dock

### 修改Finder中文件夹显示语言

    # 以Desktop为例
    touch ~/Desktop/.localized
    chmod 600 ~/Desktop/.localized

## 常用快捷键

### Chrome

- 切换用户 `Command + shift + M`
