# WPS

# 打包服务器环境



1、安装打包工具

pip install conda-pack



2、打包环境

conda pack -n my_env



3、目标服务器上解压

mkdir -p my_env

tar -xzf my_env.tar.gz -C my_env



4、查看对不对

执行python      ./my_env/bin/python

                           import torch

                           torch.cuda.is_available()

进入环境source my_env/bin/activate



5、添加到conda的虚拟环境中

conda config --add envs_dirs /home/yujiandong

conda env list

conda activate torch1.8



链接: https://pan.baidu.com/s/16fDvY6LaG5R8MGZZtQuBkg?pwd=gkkp 提取码: gkkp 复制这段内容后打开百度网盘手机App，操作更方便哦



# 服务器上传到github



1、配置身份信息



git config --global user.name  “yujiandong”

git config --global user.email  “yujiandong2025@163.com”

git config --list



2、生成公私钥

ssh-keygen -t rsa -C "yujiandong2025@163.com"

cd ~/.ssh

cat id_rsa.pub    查看公钥



3、github绑定身份

account   ->     SSH and GPG keys   ->   new ssh key

title随便填

公钥复制进去



4、验证是否成功

ssh -T git@github.com



5、将github仓库下载到本地

git clone https://github.com/yujiandong0002/WPS.git



6、将想上传的文件拷贝到克隆下来的文件夹

cp 

执行一遍添加文件git add xx

查看缓存区的内容git status



6、提交到本地仓库

git commit -m "提交信息"



7、push


