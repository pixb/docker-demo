# 我的archlinux

FROM archlinux
MAINTAINER pix<pixboly@gmail.com>

# 更新系统
RUN pacman -Syyu --noconfirm

# 安装必要软件包
RUN pacman -S iputils --noconfirm
RUN pacman -S net-tools --noconfirm
RUN pacman -S proxychains --noconfirm
RUN pacman -S neovim --noconfirm
RUN pacman -S sudo --noconfirm
RUN pacman -S git --noconfirm
RUN pacman -S openssh --noconfirm

# config ssh service
RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_dsa_key
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key
RUN /usr/sbin/sshd

# 添加用户
RUN useradd -m -s /bin/bash pix  
RUN usermod -a -G wheel pix

