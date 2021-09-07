# iterm2-zmodem


### 安装lrzsz
```
brew install lrzsz
```


### 将两个sh 脚本保存在 /usr/local/bin/
```
sudo cp ~/iterm2-zmodem-master/iterm2-* /usr/local/bin
sudo chmod 777 /usr/local/bin/iterm2-*
```


### 在iTerm 2添加Triggers
```
Regular expression: rz waiting to receive.\*\*B0100
Action: Run Silent Coprocess
Parameters: /usr/local/bin/iterm2-send-zmodem.sh

Regular expression: \*\*B00000000000000
Action: Run Silent Coprocess
Parameters: /usr/local/bin/iterm2-recv-zmodem.sh
```
![item2配置](https://github.com/vjudge/iterm2-zmodem/blob/main/item2-cfg.webp)


### 使用方法
* 将文件传到远端服务器：rz
* 将文件从远端服务器下载: sz 文件名
