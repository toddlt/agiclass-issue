# agiclass-issue

## 资料链接

AGI课程使用手册：

https://agiclass.feishu.cn/wiki/EztTwL9wniRVXXkW8itcvdyFnhc

## FAQ

### pip装包失败

1. 确认自己的python不要是最新，建议不高于3.11，不然有些软件包还未来得及适配
2. 确认本地网络是不是有问题，默认的源在国外，建议选一个国内源 https://mirrors.tuna.tsinghua.edu.cn/help/pypi/

```base
# 临时使用
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package
# 设为默认
python -m pip install --upgrade pip
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

### 装完openai包在运行时提示找不到

确认运行时配置的python环境与pip安装依赖时的python环境是同一个
