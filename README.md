# 123云盘 下载工具

## 项目介绍

123Pan 下载工具是一个使用 Python 编写的脚本，通过模拟安卓客户端协议来绕过 123Pan 的下载流量限制。该工具可以帮助用户在 Windows 系统上方便地下载 123Pan 上的文件，并提供了多种操作功能，如列出文件、下载文件、上传文件、分享文件等。

## 功能特点

- **登录**：使用用户名和密码登录 123Pan 账号。
- **列出文件**：显示当前目录下的所有文件和文件夹。
- **下载文件**：通过模拟安卓客户端协议下载文件，绕过流量限制。
- **上传文件**：将本地文件上传到 123Pan。
- **分享文件**：生成文件分享链接。
- **删除文件**：删除指定的文件或文件夹。
- **创建文件夹**：在当前目录下创建新文件夹。

## 使用方法

### 环境准备

1. 确保已安装 Python 3.x。

2. 安装所需的 Python 库：

   ```bash
   pip install requests
   ```

### 配置文件

在首次运行脚本时，会自动生成一个 `123pan.txt` 文件，用于保存用户的登录信息。请确保该文件与脚本在同一目录下。

### 运行脚本

​	可以直接下载release的可执行文件运行或运行python脚本。

​	脚本运行：

1. 克隆或下载本项目代码到本地。

2. 打开终端或命令提示符，进入项目目录。

3. 运行脚本：

   使用安卓客户端协议
   ```bash
   python android.py
   ```

​	使用web协议 

   ```bash
   	python 123pan.py
   ```

### 命令

- **登录**：`log`
- **列出文件**：`ls`
- **刷新目录**：`re`
- **下载文件**：`download <文件编号>`
- **获取下载链接** `link <文件编号>`
- **分享文件**：`share`
- **删除文件**：`delete <文件编号>`
- **创建文件夹**：`mkdir <文件夹名称>`
- **切换目录**：`cd <目录编号>` 或 `cd ..` 返回上一级目录
- **上传文件**：`upload`，然后输入文件路径
- **退出**：`exit`

### 示例

1. 登录：

   ```bash
   > log
   ```

2. 列出文件：

   ```bash
   > ls↵
   ```

3. 下载文件：

   ```bash
   > download 1↵
   ```

   或直接输入文件编号：

   ```bash
    >54↵
   1.20.0.01_v8a.apk  193.53M
   press 1 to download now: 1↵
   1.20.0.01_v8a.apk    193.53M
    [██████████████████████████████████████████████████] 100%  
   ok
   ```

   

4. 获取下载链接

   ```bash
    >link 32
   https://1-180-24-9.pd1.cjjd19.com:30443/(A Long Link)
   ```

   获取下载链接后可以使用IDM下载

5. 分享文件：

   ```bash
    >share↵
   分享文件的编号：58↵
   ['Something.jpg']
   输入1添加文件，0发起分享，其他取消0↵
   提取码，不设留空：↵
   ok
   分享链接：
   https://www.123pan.com/s/(someting)提取码：(something)
   ```

6. 删除文件：

   ```bash
   > delete 1
   ```

7. 创建文件夹：

   ```bash
   > mkdir 新建文件夹
   ```

8. 上传文件：

   ```bash
    >upload
   请输入文件路径：C:\(some path)\config
   文件名: config
   检测到1个同名文件,输入1覆盖，2保留两者，0取消：2
   上传文件的fileId: (someThing)
   已上传：100.0%
   处理中
   上传成功
   ```

## 注意事项

- 请确保在使用过程中网络连接正常。
- 由于使用了模拟安卓客户端协议，可能会有一定的风险，请谨慎使用。
- 本工具仅供学习和研究使用，请勿用于非法用途。

