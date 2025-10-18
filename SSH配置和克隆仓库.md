SSH配置(生成**id_rsa.pub**和**id_rsa.pub**(默认)密钥文件)
```
ssh-keygen -t rsa -b 4096
```
如果要添加多个密钥文件(如**test**)，则要在添加.ssh中添加配置文件**config**：
```
Host github.com  # 一个易于识别的别名(个人决定)
HostName github.com # 指定服务器地址
PreferredAuthentications Publickey # SSH认证时优先使用公钥认证
IdentityFile ~/.ssh/id_rsa # 指明私钥文件路径
```
克隆仓库
```
git clone git@密钥别名(一般为github.com):远程地址
例子 git clone git@github.com:username/repo.git
```