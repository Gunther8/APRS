# APRS Weather Station

## 项目简介
本项目是一个基于 Python 的 APRS 气象站，定期从 OpenWeather API 获取天气数据，并将其发送到 APRS-IS 服务器。该项目适用于业余无线电爱好者，特别是 APRS 用户。

## 功能特点
- 通过 OpenWeather API 获取实时天气数据（温度、湿度、风速、风向）。
- 采用 APRS 协议格式化天气数据并上传到 APRS-IS 服务器。
- 采用 TCP/IP 连接 `rotate.aprs2.net:14580` 服务器进行数据上传。
- 采用 10 分钟间隔定期发送数据。

## 先决条件
在运行本项目之前，请确保已安装以下软件和库：

### 软件要求
- Python 3.x

### 依赖库
使用以下命令安装所需依赖项：
```sh
pip install requests
```

## 配置
在 `aprs_weather.py` 文件中，修改以下配置项以匹配您的设置：

```python
CALLSIGN = "BI3MCY-10"  # 你的APRS呼号
PASSCODE = "******"  # 你的APRS-IS passcode
SERVER = "rotate.aprs2.net"  # APRS-IS服务器
PORT = 14580  # 服务器端口
LATITUDE = *   # 纬度
LONGITUDE = * # 经度
OPENWEATHER_API_KEY = "******"  # 你的OpenWeather API密钥
```

## 运行方法
确保 Python 及依赖已安装后，使用以下命令运行程序：
```sh
python aprs_weather.py
```

## 示例数据包
以下是一个示例 APRS 数据包：
```
BI3MCY-10>APRS,TCPIP*:@181230z0256.90N/12210.08E_040/015g...t068h75b10132 Airports WX in Python | gang8848@gmail.com
```



