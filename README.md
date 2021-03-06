gmo-boot-demo01
===============

This repo is gmo boot camp demo01.
https://github.com/naototty/gmo-boot-demo01

wiki
https://github.com/naototty/gmo-boot-demo01/wiki


# demo03: Reverse Proxy
## 1) destroy demo02 vm
~~~ bash
  vagrant destroy
~~~

## 2) git checkout R_demo03_1 branch
~~~ bash
  pwd

  git checkout R_demo03_1

  ls 
~~~


# demo02: Virtual Host
## 1) destroy demo01 vm
~~~ bash
  vagrant destroy
~~~
  
## 2) git checkout R_demo02_1 branch
~~~ bash
  pwd

  git checkout R_demo02_1

  ls 
~~~

## 3) vagrant up demo02 vm
~~~ bash
  vagrant up
~~~


# demo01: Virtual Machine

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

powershellのwindowを開き直すことで、sshのpathが通っている状態の端末となる

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

  git checkout R_demo01_1_01
~~~

## 12) vagrant up "demo01" server (32bit)
~~~ bash

  vagrant up
~~~

## 13) view http://192.168.33.11/ on Remote Desktop environment web browser
  うまく起動まで行けば、つぎのURLでwebが立ち上がり、phpのphpinfo()の実行を確認できる 
 
  http://192.168.33.11/


## 14) ssh web server
~~~ bash

  vagrant ssh node1
  sudo su -
~~~

or 

~~~ bash

  ssh -l vagrant 192.168.33.11
  sudo su -
~~~


# Reference URL
  * qitta.com Vagrantチュートリアル手習い http://qiita.com/naoiwata/items/2502b81f5ee940e6db8b
  * qiita.com Vagrantの基本 http://qiita.com/kidachi_/items/e63c1607705178aa257c
  * qitta.com Vagrant入門 http://qiita.com/MasayaMizuhara/items/791c2b713ac7d8c98123
  * qitta.com Vagrantコマンド詳細 http://qiita.com/yuma_iwasaki/items/988e8d66aa067fef2033
  * qitta.com Vagrant設定をいろいろ調べて(試してみた) http://qiita.com/ryurock/items/91df14537512c03488ac
  * qitta.com Windowsの環境変数をPowerShellで書き換える http://qiita.com/mmorita/items/4c44363faf74a7105199


