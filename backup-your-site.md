# 如何备份你的站点

## 使用 B2 Cloud Storage

在使用这个脚本之前你需要注册一个 [B2 Cloud Storage](https://www.backblaze.com/b2/cloud-storage.html) 账号，然后就是创建一个 Bucket 和应用密钥。

首先下载脚本

```
wget https://raw.githubusercontent.com/M1Screw/Airport-toolkit/master/b2_backup.sh
chmod +x b2_backup.sh
```

然后跑一下脚本初始化
```
./b2_backup.sh init
```

然后下载默认配置文件

```
wget https://raw.githubusercontent.com/M1Screw/Airport-toolkit/master/b2_backup_config
```

修改其中的配置，然后将配置文件修改为一个合适的名字，比如 sspanel_backup_config，将其放到跟脚本同一个目录下，然后运行脚本

```
./b2_backup.sh backup sspanel_backup_config
```

你还可以将备份任务添加到 cron 定时运行

```
1 0 * * * /usr/bin/bash /path/to/script/b2_backup.sh backup sspanel_backup_config
```
