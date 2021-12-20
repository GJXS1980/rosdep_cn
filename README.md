# rosdep init
1.创建20-default.list文件
```bash
# 进入sources.list.d
cd /etc/ros/rosdep/sources.list.d
# 创建20-default.list文件
sudo touch 20-default.list
# 编写20-default.list文件
sudo gedit 20-default.list
```

复制粘贴下面内容到20-default.list：

```bash
# os-specific listings first
yaml https://raw.github.com/ros/rosdistro/master/rosdep/osx-homebrew.yaml osx

# generic
yaml https://raw.github.com/ros/rosdistro/master/rosdep/base.yaml
yaml https://raw.github.com/ros/rosdistro/master/rosdep/python.yaml
yaml https://raw.github.com/ros/rosdistro/master/rosdep/ruby.yaml
gbpdistro https://raw.github.com/ros/rosdistro/master/releases/fuerte.yaml fuerte

# newer distributions (Groovy, Hydro, ...) must not be listed anymore, they are being fetched from the rosdistro index.yaml instead
```

# rosdep update
下载[rosdep.zip](https://github.com/GJXS1980/rosdep_cn/releases/download/v1.0/rosdep.zip)文件，然后解压到<code>~/.ros/</code>,配置完成。
