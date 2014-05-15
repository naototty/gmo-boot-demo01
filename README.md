gmo-boot-demo01
===============

This repo is gmo boot camp demo01.
https://github.com/naototty/gmo-boot-demo01

## 1) go http://conoha.macpoi.me/demo/

## 2) click "setup-cinst.bat" and download

  file url : http://conoha.macpoi.me/demo/demo01-vagrant-512mb/

  url : http://conoha.macpoi.me/demo/demo01-vagrant-512mb/setup-cinst.bat

## 3) open setup-cinst.bat file and execute
  Enter key and go.
  
## 4) open power shell
~~~ bash
  choco /?
~~~

## 5) test install; google chrome
~~~ bash
  choco list chrome
  choco install GoogleChrome
~~~

## 6) install VirtualBox
~~~ bash
  choco list VirtualBox
  choco install VirtualBox VirtualBox.ExtensionPack vagrant Wget
~~~

## 7) install git command
~~~ bash
  choco list git
  choco install git git.commandline git.install hosts.editor
~~~

## 8) install putty, ssh
~~~ bash
  choco list ssh
  choco install putty.install
~~~
and close power shell window.


## 9) install openssh (ssh command client for power shell)
execute Windows PowerShell with Administrator roles

open new Administrator powershell : "管理者として実行する"
~~~ bash
Windows PowerShell
Copyright (C) 2013 Microsoft Corporation. All rights reserved.

PS C:\Windows\system32> $path = [Environment]::GetEnvironmentVariable('PATH', 'Machine')
PS C:\Windows\system32> $path += ';' + 'C:\git\bin'
PS C:\Windows\system32> [Environment]::SetEnvironmentVariable('PATH', $path, 'Machine')
PS C:\Windows\system32>
~~~
and close AlL power shell window.
  
open new power shell

## 10) make Hands on "demo01" work dir
~~~ bash
  mkdir devel
  cd devel
  mkdir demo01
  cd demo01
  pwd
~~~


## 11) git clone "demo01" hands on environment
~~~ bash
  git clone https://github.com/naototty/gmo-boot-demo01.git

  ls 

  cd gmo-boot-demo01
~~~

## 12) vagrant up "demo01" server (32bit)
~~~ bash

  vagrant up
~~~
