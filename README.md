Vagrant Ansible Example
=======================

Vagrant で Ansible Provision を使って Sinatra アプリを動かすサンプル

https://github.com/algas/vagrant-ansible-example

## Dependencies

以下の２つをあらかじめインストールしておいてください。

* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

## Usage

1. Ansible のインストール    
`pip install ansible`
2. Repository の取得  
`git clone https://github.com/algas/vagrant-ansible-example.git`
3. Vagrant 実行  
`cd vagrant-ansible-example && vagrant up`
4. 実行確認  
`curl -v http://localhost:25000/hello`


## Structure

* ansible.cfg: Ansibleの環境設定
* hello.rb: Sinatraのスクリプト
* hosts: デプロイ先の設定
* sinatra.yml: Ansibleのメインファイル
* ssh.config: SSHの設定
* Vagrantfile: Vagrantの設定
