
# python
-  date\open\json..
- pytest
- unnitest

# java
 junit、redis、mq、netty

# sql
- mysql
- postgresql
- mongodb
- sql server

# selenium :web自动化测试 
	driver、等待、xpath、By、Actions、keyboard、Router、remote
	
## robot framework 
	- .robot .resource .py 
	- ride
	
## appium  移动端自动化测试
	
## load runner 应用负载、压力、性能自动化测试工具 
 
## Cypress UI自动化测试框架

# 自动化测试实践
- 数据驱动
- 页面对象模型（PO）

# git
 git init 、 git clone、  git add 、 git commit(-m 'msg')、 git pull、 git push、  git branch、   git checkout、 git cheery-pick 、 git history 
  
# 软件工程
	- 模型
	- 软件测试流程
	- 需求分析


# linux
	- ps grep tail head top free nvidia-smi cat  cd ls ll "fileOpreation" tar 
	

# 网络协议
    - http
    - udp
	- socket
	- RESTful API
		Morest
	- SOAP/REST
# GPU、显卡
    nvidia-smi
    CUDA驱动

# 测试基础
- 功能测试
- ut测试  pytest、 unittest 、junit
- 用例管理 jira 禅道 ones


# 测试管理
  - 文档管理
	用例（评审）、自动化用例、汇报报告
  - 缺陷管理
    > bug提交：复现步骤、结果、期望、测试环境、附件
    > bug验证：验证结果、验证版本、评论意见、测试用例
    > bug严重级别：紧急、严重、普通、微小
    > bug优先级：高、中、低
    > bug状态：激活、待解决、已解决、关闭
 - 测试规范管理  
	<details>
    1、接口自动化测试过程：  
        接口管理-场景管理-测试用例编写-单接口自动化测试用例编写-场景（多接口）自动化测试用例编写-接口自动化测试用例执行-数据度量  
    2、要求：    
        接口管理：分级管理，标注核心接口，区分优先级，梳理需要的接口测试用例
        场景管理：场景评审  
        接口自动化用例：评优先级，编写用例   
        场景自动化测试用例编写：覆盖正向业务流程、提取公共变量集、前置处理数据准备、后置数据清理、结果校验、里程碑校验  
        场景自动化用例执行：执行周期、持续集成、结果分析 
	</details>
	
  - 测试代码管理
  
  - 测试排期、工作量评估
  
# 测试报告

- 显存测试报告内容
   测试报告一般包括：测试目的、测试人员、日期、测试环境（ip\cpu\gpu\内存\分辨率）、测试场景（操作类型、并发数、显存占用、内存占用、网络带宽、数据等）、测试指标 、测试结果（前置条件、具体测试版本、具体配置）、结论（性能瓶颈、调整内容及效果、性能优化效果）
   
- 自动化生成测试报告
   HTMLTestRunner、allure
   
# postman /apifox
- pm
- xMySQL

# jmeter
 - beanshell
 
# 云平台
- k8s
	rancher
	IDC
	kubctrl
	
- docker
	
	
# CI/CD

- GitHub Actions
- docker
	docker exec、docker logs 
	
## jenkins

# 测试自动化管理平台
- Katalon、LambdaTest、Perfecto、Zebrunner 
- Cucumber 行为驱动开发（BDD）

# 压测/性能测试
- 磁盘性能测试：  fio、dd命令  [FIO博文](https://www.cnblogs.com/lyhabc/p/16708771.html)  
	吞吐量： 顺序读 顺序写 顺序混合读写 随机读  随机写 随机混合读写
	IOPS
- 显存占用测试：
- 内存占用测试：
- cpu性能测试

## 性能需求指标


# 接口测试
# 安全测试
	漏洞扫描、密码加密、url免登陆访问攻击、fildder
	[安全测试概念](https://www.cnblogs.com/Jcloud/p/16669942.html)

# 监控
- nmon
- cat
- grafana

# 测试工具
[nmon for linux](http://nmon.sourceforge.net)
<details>
-  常用监测:
        CPU 使用率
        内存使用情况
        内核统计信息和运行队列信息
        磁盘 I/O 速度、传输和读/写比率f
        文件系统中的可用空间
        磁盘适配器

    -  nmon 快捷键  
            q : 停止并退出 nmon  
            h : 查看帮助  
            c : 查看 CPU 统计数据  
            m : 查看内存统计数据  
            d : 查看硬盘统计数据  
            k : 查看内核统计数据  
            n : 查看网络统计数据  
            N : 查看 NFS 统计数据  
            j : 查看文件系统统计数据  
            t : 查看高耗进程  
            V : 查看虚拟内存统计数据  
            v : 详细模式  

    - 数据收集
        性能测试时，需要根据测试场景的执行情况，分析一段时间内系统资源的变化，这时需要nmon采集数据并保存下来，以下是常用的参数：  
        -f 参数:生成文件,文件名=主机名+当前时间.nmon  
        -T 参数:显示资源占有率较高的进程  
        -s 参数:-s 10表示每隔10秒采集一次数据  
        -c 参数:-s 10表示总共采集十次数据  
        -m 参数:指定文件保存目录  
        eg：每5秒采集一次，一共采集12次（即一分钟的数据） nmon -f -s 5 -c12 -m /home/Desktop 
        
    - 数据分析
        借助nmon analyser可以把nmon采集的数据生成直观的Excel表，nmon analyser可以在IBM的官网下载[https://www.ibm.com/developerworks/community/wikis/home?lang=en#!/wiki/Power+Systems/page/nmon_analyser]
        在windows上下载后解压，有word和exce两个文档，Word是说明文档，包括更新日志，详细参数等，其中的Excel就是nmon analyser工具  
        注：免费版WPS，没有包含宏，需要安装宏插件(VBA for WPS)，Excel是自带宏插件的，如果宏不能运行，需要做以下操作：工具 -> 宏 -> 安全性 -> 中，然后再打开文件并允许运行宏。
</details>


# 弱网模拟 
clumsy  
WANem  
Fiddler  
http://www.51ste.com/share/det-825.html
> 当被 filter 的网络数据包被拦截后，你可以选择 clumsy 提供的功能来有目的性的调整网络情况：  
> 延迟 (Lag)，把数据包缓存一段时间后再发出，这样能够模拟网络延迟的状况。   
> 掉包 (Drop)，随机丢弃一些数据。   
> 节流 (Throttle)，把一小段时间内的数据拦截下来后再在之后的同一时间一同发出去。   
> 重发 (Duplicate)，随机复制一些数据并与其本身一同发送。   
> 乱序 (Out of order)，打乱数据包发送的顺序。   
> 篡改 (Tamper)，随机修改小部分的包裹内容。   


# devops 

# mock数据


#AI 
- 语音 、计算机视觉
  opencv、  NLP
  
# 常被忽略
 - 缺陷分析 
 - 用例评审
 - 测试计划
 
# http/rpc/websocket

