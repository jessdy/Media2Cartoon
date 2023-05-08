# Media2Cartoon

[**English**](./README.md) | [**中文简体**](./README_zh_CN.md)

This is an open source software that can convert uploaded images or videos into cartoon style.

![screenshot](screenshot.png)

## Features

- Supports uploading of image and video formats
- Supports resizing video.
- Supports trimming video length.

## Usage

### Docker（Recommend）

1. Clone the code repository to your local machine.

```
git clone https://github.com/jessdy/Media2Cartoon.git
```


2. Container building

```sh
docker build -t Media2Cartoon:1.0 .
```


3. Start the container

```sh
docker run -d --name cartoon-1.0 -p 18080:18080 Media2Cartoon:1.0
```


4. Visit

- URL：[http://localhost:18080/front/]

###  Local

1. Clone the code repository to your local machine.

```
git clone https://github.com/jessdy/Media2Cartoon.git
```

2. Install dependencies

```cmd
cd server
pip uninstall -y protobuf
pip install protobuf==3.19.0 -i https://pypi.douban.com/simple      
pip install -r requirements.txt -i https://pypi.douban.com/simple 
uvicorn main:app --reload --port 18080 --host 0.0.0.0

```

3. Visit

- URL：[http://localhost:18080/front/]