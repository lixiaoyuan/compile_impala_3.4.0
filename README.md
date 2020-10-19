# compile_impala_3.4.0

编译步骤：https://blog.csdn.net/huang_quanlong/article/details/106868826

# 1、bin/bootstrap_system.sh 
  替换  

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



# 2、使用strip 压缩编译后的impalad
