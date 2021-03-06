# [安装与架设](../)/Minecraft Bukkit 服务端

## 概述
- JustChat 的 Bukkit / Spigot 端插件。

## 安装
1. [下载插件](https://github.com/ParaParty/JustChat/releases/)
1. 复制到 [Bukkit](https://bukkit.org/)/Spigot(https://spigotmc.org/)插件目录
1. 重启一次 Bukkit/Spigot ，使得插件生成插件配置文件
1. 使用 [notepad++](https://notepad-plus-plus.org/) 或 [Sublime Text](http://www.sublimetext.com/) 或 记事本 或 gedit 或 vim 等文本编辑器修改**并保存**配置文件
1. 重启 Bukkit/Spigot ， 使得修改后的配置文件生效。

## 配置文件 
- 配置文件 `config.yml`
```yaml
############### 服务器设置 ###############
#服务器IP
serverIP: "mcserver.example.com"

#服务器端口，默认38440
serverPort: 38440

#本终端名称
Name: "Bukkit"

#本终端编号
ID: "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

#-----------开发设置----------#
#！！！非必要请勿改动！！！
#服务器心跳速度（秒）
#需要与PHP服务器的心跳同时修改
serverPulse: 20

############### 扩展插件 ##################
#是否使用VexView插件来显示图片
#需要付费版的VexView才能使用
useVexView: true

#收到图片时显示在屏幕的位置x
#需要VexView插件支持
#这个值需要在0和1之间，它是你屏幕从左到右的百分比宽度
imageX: 0.68

#收到图片时显示在屏幕的位置y
#需要VexView插件支持
#这个值需要在0和1之间，它是你屏幕从上到下的百分比高度
imageY: 0.65
```

## 指令
### `/multirobot`
- 介绍 : 主指令
- 用法 : `/multirobot`

### `/multirobot:info`
- 介绍 : 发送一条消息到群里
- 用法 : `/multirobot:info 消息内容`
- 权限 : `multirobot.forward.chat`
- 
### `/multirobot:qq`
- 介绍 : 开启或关闭QQ消息，服务器重启后设置清空
- 用法 : `/multirobot:qq`
- 权限 : 所有玩家

## 权限
| 权限 | 说明 |
|:----|:-----|
|`multirobot.admin`|管理员设置指令（暂无）|
|`multirobot.forward.chat`|允许将聊天信息发送到QQ群|
|`multirobot.forward.network.*`|允许将上下线信息发送到QQ群|
|`multirobot.forward.network.join`|允许将上线信息发送到QQ群|
|`multirobot.forward.network.disconnect`|允许将下线信息发送到QQ群|
|`multirobot.forward.death`|允许将游戏角色死亡信息发送到QQ群|
