# 目的

Ansibleを使って
Ubuntu 18.04上にdockerとdocker-composeをセットアップします。

ハンズオン目的で準備したものなので、プロダクションでの利用は意図していません。

## 使い方

### 1. inventory/inventory.iniを修正

`inventory.ini`を要件に合わせて編集します。

```ini
[docker]
192.168.56.101
```

### 2. デプロイ

```console
$ ansible-playbook -i inventory/inventory.ini playbook/main.yml
```

## 注意点

+ ansibleのsshユーザがdockerグループに所属するので注意
