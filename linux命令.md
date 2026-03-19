

# 🔹 1. 文件与目录操作

```bash
# 查看当前目录
pwd

# 显示目录内容
ls
ls -l        # 详细信息
ls -a        # 包括隐藏文件
ls -lh       # 人性化显示大小

# 切换目录
cd /home     # 进入目录
cd ..        # 返回上一级
cd -         # 返回上一次路径

# 创建目录
mkdir mydir
mkdir -p a/b/c  # 递归创建

# 删除目录
rmdir mydir       # 删除空目录
rm -rf mydir      # 删除目录及内容

# 创建文件
touch file.txt

# 复制文件/目录
cp file1 file2
cp -r dir1 dir2   # 复制整个目录

# 移动/重命名
mv old.txt new.txt
mv file.txt /tmp/

# 删除文件
rm file.txt
```

---

# 🔹 2. 文件查看与编辑

```bash
# 查看文件内容
cat file.txt
tac file.txt     # 反向显示
more file.txt    # 分页查看
less file.txt    # 支持上下翻页/搜索

# 查看前/后几行
head -n 10 file.txt
tail -n 20 file.txt
tail -f log.txt  # 实时查看日志

# 编辑文件
nano file.txt
vim file.txt
```

---

# 🔹 3. 文件搜索

```bash
# 查找文件
find / -name "file.txt"
find . -type f -name "*.cpp"

# 文本搜索
grep "hello" file.txt
grep -r "main" ./src   # 递归搜索
grep -n "error" log.txt # 显示行号

# 模式匹配
locate test.txt
updatedb   # 更新 locate 数据库
```

---

# 🔹 4. 权限管理

```bash
# 查看权限
ls -l

# 修改权限
chmod 755 script.sh
chmod u+x file.sh  # 给用户加执行权限

# 修改属主/属组
chown user file.txt
chown user:group file.txt
```

---

# 🔹 5. 压缩与解压

```bash
# tar 打包
tar -cvf archive.tar file1 file2
tar -xvf archive.tar

# tar.gz 压缩
tar -czvf archive.tar.gz dir/
tar -xzvf archive.tar.gz

# zip 压缩
zip archive.zip file1 file2
unzip archive.zip
```

---

# 🔹 6. 系统信息

```bash
# 系统版本
uname -a
cat /etc/os-release

# CPU / 内存
top
htop        # 更友好（需安装）
free -h
df -h       # 磁盘使用情况
du -sh *    # 目录大小

# 进程
ps aux
ps -ef | grep nginx
kill -9 PID   # 强制杀死进程
```

---

# 🔹 7. 网络相关

```bash
# IP 地址
ifconfig       # (老命令)
ip addr show   # 推荐

# 测试连通性
ping www.baidu.com
curl http://example.com
wget http://example.com/file.txt

# 端口占用
netstat -tulnp
ss -tulnp     # 推荐
```

---

# 🔹 8. 用户管理

```bash
# 添加/删除用户
useradd testuser
passwd testuser
userdel -r testuser

# 切换用户
su - testuser
whoami
```

---

# 🔹 9. 软件包管理

（以 **Ubuntu/Debian** 为例）

```bash
# 更新软件源
sudo apt update

# 安装软件
sudo apt install vim

# 卸载软件
sudo apt remove vim

# 搜索软件
apt search nginx
```

（**CentOS/RHEL** 用 `yum` / `dnf`）

---

# 🔹 10. 其他常用命令

```bash
# 清屏
clear

# 输出内容
echo "Hello Linux"

# 查看日期
date

# 查看日历
cal

# 查看命令路径
which python
whereis gcc

# 历史命令
history
!100   # 执行第100条命令
```

---

要不要我帮你整理成一个 **Linux 命令对照表（PDF/Markdown）**，分类清晰，还能打印出来当小抄？