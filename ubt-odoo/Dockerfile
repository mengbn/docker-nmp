FROM    centos:6.7
MAINTAINER  liumeng "759498475@qq.com"

RUN    /bin/echo 'root:123456' |chpasswd
RUN    useradd five3
RUN    /bin/echo 'five3:123456' |chpasswd
RUN    /bin/echo -e "LANG=\"en_US.UTF-8\"" >/etc/default/local
EXPOSE    22
EXPOSE    80
CMD    /usr/sbin/sshd -D
