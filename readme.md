1.解压文件。
2.在用户根目录下，编辑.brashrc文件，加入tprofiler的环境变量。
# set params of tprofiler
export TPROFILER_HOME=/home/cenxin/tprofiler  这是解压的文件夹的路径
export TPROFILER_HOST=127.0.0.1  系统的ip
export TPROFILER_PORT=50001  tprofiler要占用的端口

export PATH=$JAVA_HOME/bin:$PATH:$NODE_HOME/bin:$TPROFILER_HOME/bin:$PATH

3.在jvm启动参数中添加参数：
-javaagent:${TPROFILER_HOME}/lib/tprofiler.jar 
-Dprofile.properties=${TPROFILER_HOME}/profile.properties