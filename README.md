# compile_impala_3.4.0

编译步骤：
https://blog.csdn.net/huang_quanlong/article/details/106868826
https://cwiki.apache.org/confluence/display/IMPALA/Building+Impala

# 1、bin/bootstrap_system.sh 
  查找下载apache-ant位置，替换为下面地址

```shell
  redhat sudo wget -nv \
        https://archive.apache.org/dist/ant/binaries/apache-ant-1.9.14-bin.tar.gz
redhat sudo sha512sum -c - <<< '487dbd1d7f678a92924ba884a57e910ccb4fe565c554278795a8fdfc80c4e88d81ebc2ccecb5a8f353f0b2076572bb921499a2cadb064e0f44fc406a3c31da20  apache-ant-1.9.14-bin.tar.gz'
```

# 2、bin/bootstrap_toolchain.py
  开始地方添加 

```shell
import sys
reload(sys)
sys.setdefaultencoding('utf-8')
```

# 3、开始编译
    参考编译步骤连接
    
# 4、使用strip 压缩编译后的impalad
