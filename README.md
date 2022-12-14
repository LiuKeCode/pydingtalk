# PyDingTalk
[![GitHub issues](https://img.shields.io/github/issues/liukecode/pydingtalk)](https://github.com/liukecode/pydingtalk/issues)
[![GitHub forks](https://img.shields.io/github/forks/liukecode/pydingtalk)](https://github.com/liukecode/pydingtalk/network)
[![GitHub stars](https://img.shields.io/github/stars/liukecode/pydingtalk)](https://github.com/liukecode/pydingtalk/stargazers)
[![GitHub license](https://img.shields.io/github/license/liukecode/pydingtalk)](https://github.com/liukecode/pydingtalk/blob/main/LICENSE)
[![contributors](https://img.shields.io/github/contributors/liukecode/pydingtalk)](https://github.com/liukecode/pydingtalk/graphs/contributors)
[![PyPI](https://img.shields.io/pypi/v/pydingtalk)](https://pypi.org/project/pydingtalk/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/pydingtalk)](https://pypi.org/project/pydingtalk/)
[![Downloads](https://pepy.tech/badge/pydingtalk/month)](https://pepy.tech/project/pydingtalk)

This is a msg-robot for [DingTalk](https://open.dingtalk.com/document/robots/custom-robot-access)

## Install
```
python -m pip install pydingtalk
```
## Getting Started
send text msg
```
import pydingtalk

token = "c30*****71"
key = "SEC*****"
bot = pydingtalk.Bot(token, key)
data = {"msgtype": "text","text": {"content":"LiuKeTest"}}
bot.bot_send(data)

# @ user
# data = {"at": {"atMobiles": ["18xxx", "13xxx"]}, "msgtype": "text","text""": {"content":"LiuKeTest"}}
# @ all user
# data = {"at": {"isAtAll": True}, "msgtype": "text","text""": {"content":"LiuKeTest"}}
bot.send_msg(msg, 'chat_id'))
```
send link
```
data = {"msgtype": "link", "link": {"text":"LiuKeTest", "title": "Test", "picUrl": "https://xxx", "messageUrl": "https://xxx"}}
```

send link
```
data = {"msgtype": "markdown", "markdown": {"title": "LiuKeTest", "text": "### LiuKeTest @138XXXXXXXX \n > [pydingtalk](https://pypi.org/project/pydingtalk)"}}
```
More message types, please visit [DingTalk](https://open.dingtalk.com/document/robots/custom-robot-access).

## Features
- Supports all types message 


## Contributing

Contributions are welcome.<br/>
If you've found a bug within this project, please open an issue to discuss what you would like to change.<br/>
If it's an issue with the API, please report any new issues at [pydingtalk issues](https://github.com/liukecode/pydingtalk)