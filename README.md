# kerberos-network-packets
在学习kerberos交互过程中，wireshark抓取的kerberos交互的流量以及相关流量解密的keytab

kerberos.pcapng是整个完整的Kerberos协议交互过程中的流量。

bob.keytab 是使用bob用户的hash进行解密的keytab
cifs_bob.keytab 是使用cifs服务hash进行解密的keytab
krbtgt.keytab 是使用krbtgt账户hash进行解密的keytab

keytab直接使用wireshark进行导入，即可解密kerberos流量中的加密部分，查看解密后的字段内容。

s4u2self_kerberos.pcapng和s4u2proxy_kerberos.pcapng是基于资源的约束委派的交互的流量。

环境信息：
域控
dc.test.mydomain 192.168.233.131
bob.test.mydomain 192.168.233.132

普通域用户bob的密码qwer@1234
