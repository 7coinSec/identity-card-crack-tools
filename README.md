<h1 align="center">identity-card-crack-tools</h1>
<br>

<div align="center">
<img src="https://img.shields.io/github/pipenv/locked/python-version/metabolize/rq-dashboard-on-heroku?style=for-the-badge&logo=appveyor">
<img src="https://img.shields.io/github/stars/7coinSec/identity-card-crack-tools?style=for-the-badge&logo=appveyor">
</div>


<h3 align="center">一个用于枚举可用SFZ号的工具</h3>

<hr>
	<br>
<div align="center">
		<img width="200" src="images/logo.jpg">
</div>
<h2 align="center">该工具由7coin安全团队强力驱动</h2>
<hr>
	<br>
	<br>

## 目录

[TOC]


## 前言

一个用于枚举可用SFZ号的工具，工具原理十分简单，即使原理很简单，仍然还有一些bug，日后再做相关完善。

**注意**

- 本项目仅用于学习交流，请勿用于非法用途
- 如用于非法用法，产生的后果与本项目无关



## 用法

```sh
python3 identity-card-crack-tools.py -h

usage: identity-card-crack-tools.py [-h] [-i IDENTITY] [-y YEAR] [-o OUT]

optional arguments:
  -h, --help            show this help message and exit
  -i IDENTITY, --identity IDENTITY
                        输入待破解的身份证号，不确定字符用问号?代替
  -y YEAR, --year YEAR  e.2000 爆破2000至今的身份证号
  -o OUT, --out OUT     输出到本地文件
```

该项目提供了四种爆破方式：

1. 爆破SFZ的年份4位（需要`-y`参数）

```
python3 identity-card-crack-tools.py -i "110101????01011009" -y 2000 -o 1.txt
```

2. 爆破SFZ的月日4位（无需`-y`参数）

```
python3 identity-card-crack-tools.py -i "1101011900????1009" -o 1.txt
```

3. 爆破SFZ的年月日8位（需要`-y`参数）

```
python3 identity-card-crack-tools.py -i "110101????????1009" -y 2000 -o 1.txt
```

4. 爆破SFZ的最后4位（无需`-y`参数）

```
python3 identity-card-crack-tools.py -i "11010119000101????" -o 1.txt
```

## TODO

- 添加指定男女性别功能【TODO】
- 添加输入姓名自动识别男女爆破SFZ功能【TODO】

## 免责任声明

该工具仅供学习和参考。因用于其他用途而产生不良后果,作者不承担任何法律责任。



本工具仅能在取得足够合法授权的企业安全建设中使用，在使用本工具过程中，您应确保自己所有行为符合当地的法律法规。 如您在使用本工具的过程中存在任何非法行为，您将自行承担所有后果，本工具所有开发者和所有贡献者不承担任何法律及连带责任。 除非您已充分阅读、完全理解并接受本协议所有条款，否则，请您不要安装并使用本工具。 您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。
