# hadoop-wordcount
## 说明：
此项目是用于在不搭建分布式集群的情况下，对mapreduce程序进行编写并调试。测试成功后将项目导出jar包后放到分布式服务器上即可。
这里的wordcount使用的官方案例，可将此项目作为基础模板进行修改。

* IDE：IDEA
* 版本管理：git
* 包管理：maven

注意事项：
* 将pom.xml中的依赖包导入，运行时须配置edit configurations,新建Application，配置工作路径为 【项目路径】，配置Program arguments为 【输入文件夹 输出文件夹】input/ output/
* 运行时需要将本项目中的output文件夹删除，Hadoop会自动生成，如果存在会报错。【此时output中的文件为本示例的运行结果。】
* 若在Windows平台下运行，会遇到对文件夹操作权限不足的错误，需要将maven库中的hadoop-core-1.2.1.jar 替换为本项目中提供的同名jar包。否则可将项目中的此jar包删除。
