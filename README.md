```
get_RSA.java 用来获取公私密钥 Get RSA key
Beacon_metadata_RSA_Decrypt.py 解密元数据 Decrypt Beacon metadata
CS_Task_AES_Decrypt.py 解密CS发送任务数据 Decrypt CS sending task data
Beacon_Task_return_AES_Decrypt.py 解密Beacon任务执行结果 Decrypt the execution result of the Beacon task
```

相关参考
https://research.nccgroup.com/2020/06/15/striking-back-at-retired-cobalt-strike-a-look-at-a-legacy-vulnerability/

从序列化文件 `.cobaltstrike.beacon_keys` 获取 `PublicKey`公钥 私钥`PrivateKey`

`file .cobaltstrike.beacon_keys`

```
.cobaltstrike.beacon_keys: Java serialization data, version 5
```

#### Get key

```
javac -cp cobaltstrike.jar:. DumpKeys.java
```

```
java -cp cobaltstrike.jar:. DumpKeys
```

```
Private Key: MIICdQIBADANBgkqhkiG9w0BAQEFAASCAl8wggJbAgEAAoGBAL/j7OjJQ4FlvhYYcnRKv9cEHrWStq6bpGJsRTQbC+AWL2WuxWB2qtP6oN/hOhLFExwBKpirS7NIVSSW7FsAMl1RtNjFAtv57i9AiEDTjooMDaOn2Rsut0DWOWguIzPb0qqKQYWkQv87bf7bapj88h

Public Key: MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQC/4+IDAQAB
```
https://gist.github.com/olliencc/af056560e943bafa145120103a0947a3/raw/ccb41faee3424f83e0ab6c65ab6ce3aa0dc297bc/Dump.java
