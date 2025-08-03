# python
新建python Flask环境

将main.py requirements.txt文件上传覆盖，或者先删除再上传也可

在main.py里填写环境变量，uuid和隧道

打开devserver.sh文件，删除所有代码，然后复制以下四行代码粘贴进去  ctrl +s 保存

```
#!/bin/sh
source .venv/bin/activate
pip install -r requirements.txt
python main.py -p $PORT --debug
```

打开.idx文件夹里的dev.nix  将第7行的 `packages = [ pkgs.python3 ];` 改为 `packages = [ pkgs.python3 pkgs.openssl_3_3.bin ];`   ctrl +s 保存，右下角出现紫色 Rebuild Environment 按钮 点击会自动重新部署

信息在.cache文件夹下的sub.txt里
