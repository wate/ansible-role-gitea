gitea
=================

Setup gitea

OS Platform
-----------------

### Debian

- bullseye

Role Variables
--------------

### `gitea_version`

Giteaのバージョン

### `gitea_app_name`

Giteaのアプリケーション名

### `gitea_mode`

Giteaの動作モード  
設定値: dev / prod / test

### `gitea_internal_token`

Giteaの「INTERNAL_TOKEN」の設定値  
※未指定の場合はトークンが自動生成されます

### `gitea_lfs_jwt_secret`

Giteaの「LFS_JWT_SECRET」の設定  
※未指定の場合はトークンが自動生成されます

### `gitea_secret_key`

Giteaの「SECRET_KEY」の設定  
※未指定の場合はトークンが自動生成されます

### `gitea_cfg`

Giteaの設定  
その他の設定については以下を参照  
https://docs.gitea.io/en-us/config-cheat-sheet/  
サンプルについては以下を参照  
https://github.com/go-gitea/gitea/blob/main/custom/conf/app.example.ini

### `gitea_service_extra_cfg`

Giteaのサービス設定  
※設定のサンプルについては以下を参照  
https://github.com/go-gitea/gitea/blob/main/contrib/systemd/gitea.service

Example Playbook
--------------

```yaml
- hosts: servers
  roles:
    - role: gitea
```

License
--------------

Apache License 2.0
