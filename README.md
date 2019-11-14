监控服务器基本状态和应用存活状态。  
将应用打jar包，放入主服务器运行。  
通过在主服务器上，向其他服务器发送shell命令并获取结果，解析返回结果判断服务器的状态和服务器上应用的状态。  

例如，有5台服务器，web01,web02...05，只有01可以通过外网访问，其他都是内网访问，那么在servers.yml中配置5台服务器的信息，把jar放到01上运行。  
01会向02...05发送shell命令获取信息，然后解析，拼接成邮件内容。

![服务器分布/Servers Distribution](https://raw.githubusercontent.com/MCJIBA/server-detective/master/src/main/resources/example.jpg)