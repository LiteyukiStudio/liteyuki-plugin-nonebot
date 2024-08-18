<div align="center">
  <img src="https://cdn.liteyuki.icu/static/img/liteyuki_icon_640.png" width="180" height="180" alt="NoneBotPluginLogo">

</div>

<div align="center">

# liteyukibot-plugin-nonebot

_✨ 为轻雪机器人提供NoneBot支持 ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/LiteyukiStudio/nonebot-plugin-acgnshow.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/liteyukibot-plugin-nonebot">
    <img src="https://img.shields.io/pypi/v/liteyukibot-plugin-nonebot.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.10+-blue.svg" alt="python">

</div>

## 📖 介绍

一个简单的 liteyukibot 插件，可以为你的机器人提供 NoneBot 支持

## 💿 安装

<details open>
<summary>使用 pip 安装</summary>
在 轻雪 项目的根目录下打开命令行, 输入以下指令即可安装

    pip install liteyukibot-plugin-nonebot

</details>

<details>
<summary>使用包管理器安装</summary>
在 nonebot2 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>

    pip install liteyukibot-plugin-nonebot

</details>
<details>
<summary>pdm</summary>

    pdm add liteyukibot-plugin-nonebot

</details>
<details>
<summary>poetry</summary>

    poetry add liteyukibot-plugin-nonebot

</details>
<details>
<summary>conda</summary>

    conda install liteyukibot-plugin-nonebot

</details>
</details>



## 🎉 使用

### 仅运行此插件(开发测试)

> 运行入口文件

```shell
python main.py
```

> 或运行开发工具直接启动

```python
from liteyuki.dev.plugin import run_plugins

if __name__ == "__main__":
    run_plugins("liteyukibot_plugin_nonebot")
```

### 装载到轻雪机器人程式运行(生产环境)

在轻雪配置文件中添加以下结构配置，使轻雪知道该加载此插件

> 扁平配置项
```yaml
liteyuki.plugins: [ ..., "liteyukibot_plugin_nonebot" ]

```

或是
> 普通配置项

```yaml
liteyuki:
  plugins:
    ...
    - liteyukibot_plugin_nonebot
```

默认装载`nonebot-adapter-onebot`适配器和`fastapi`，`httpx`及`websockets`几个常用驱动器，可根据需求进行配置

安装其他NoneBot商店推荐使用轻雪的NoneBot插件`npm`

## ⚙️ 配置

参考LiteyukiBot的[配置文档](https://bot.liteyuki.icu/deploy/config.html)，在config下新建配置文件`nonebot.yml/toml/json`(你可自行命名)，填入如下结构配置文件，这里使用yaml

```yaml
nonebot:
  host: 127.0.0.1 # 监听地址，外部访问请设置为0.0.0.0
  port: 8080  # 自定义端口
  command_start: [ "", "/" ]  # 命令前缀
  superusers: [ "0000" ]  # 你的用户id
  nickname: [ "liteyuki" ]  # 你的机器人昵称
```

目前该插件已内置在[轻雪机器人应用](https://bot.liteyuki.icu)中，无需单独安装

如果你是基于[轻雪框架](https://pypi.org/project/liteyukibot/)二次开发，需要手动安装
