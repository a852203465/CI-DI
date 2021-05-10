# 搭建 自动化部署，构建服务器环境

## gitlab
修改gitlab.rb文件, 增加配置
```text
external_url 'https://10.20.1.179'
nginx['redirect_http_to_https'] =true
gitlab_rails['gitlab_shell_ssh_port'] = 2222
gitlab_rails['gitlab_ssh_host'] = '10.20.1.179'
```







































