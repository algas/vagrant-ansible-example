Vagrant Ansible Example
=======================

Vagrant で Ansible Provision を使って Sinatra アプリを動かすサンプル

https://github.com/algas/vagrant-ansible-example

## Dependencies

以下の２つをあらかじめインストールしておいてください。

* [VirtualBox](https://www.virtualbox.org/wiki/Downloads) 4.3.20
* [Vagrant](https://www.vagrantup.com/downloads.html) 1.6.5

## Usage

### 初回時

1. Ansible のインストール    
`pip install ansible`
2. Repository の取得  
`git clone https://github.com/algas/vagrant-ansible-example.git`
3. Vagrant 起動と Ansible 実行  
`cd vagrant-ansible-example && vagrant up`
4. 実行確認  
`curl -v http://localhost:25000/hello`

### ２回目以降

1. Ansible 実行  
`vagrant provision`
2. 実行確認  
`curl -v http://localhost:25000/hello`

### 終了

1. Vagrant 停止  
`vagrant halt`

## Structure

* ansible.cfg: Ansibleの環境設定
* hello.rb: Sinatraのスクリプト
* hosts: デプロイ先の設定
* sinatra.yml: Ansibleのメインファイル
* ssh.config: SSHの設定
* Vagrantfile: Vagrantの設定
