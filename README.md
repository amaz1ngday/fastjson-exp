# fastjson-exp
fastjson利用，burp插件。
支持jndi利用检测，tomcat、spring回显，哥斯拉内存马，回显利用链为dhcp、ibatis、c3p0，内存马支持tomcat89
# 用法
加载到burp插件，自行选择echo、jndi、inject

# 测试环境
tomcat启动后，将war包放在webapps目录即（tomcat自带dhcp依赖），漏洞环境为1.2.24和1.2.47。
