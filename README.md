![HT4GU%SZMQ@}2ULTMB`9X86](https://github.com/forget-eve/NSP/assets/144145556/b536a251-c50a-4f9c-8e26-dafabb087f64)# 课前须知

> [课程主页](https://faculty.ustc.edu.cn/kpxue/zh_CN/zhym/108944/list/index.htm)

- [x] 课程安排：50学时授课+6学时研讨+2学时复习
- [x] 成绩评定：
  > - 期末考试60%
  > - 平时作业25% (Project 15%，各章节作业10%)
  > - 课堂等平时表现5%+课堂测试10%(2-3次)

# 第一章：网络安全综述 

## 1.1 网络安全概述

### 网络安全事件举例

- [x] 网络监听

<p align="center">
  <img src="./img/网络监听.png" alt="网络监听">
  <p align="center">
   <span>网络监听</span>
  </p>
</p>

- [x] 假冒站点phishing

<p align="center">
  <img src="./img/假冒站点phishing.png" alt="假冒站点phishing">
  <p align="center">
   <span>假冒站点phishing</span>
  </p>
</p>

- [x] 不安全Email

<p align="center">
  <img src="./img/不安全Email.png" alt="不安全Email">
  <p align="center">
   <span>不安全Email</span>
  </p>
</p>

- [x] 抵赖

<p align="center">
  <img src="./img/抵赖.png" alt="抵赖">
  <p align="center">
   <span>抵赖</span>
  </p>
</p>

### 网络安全概述

- [x] 网络安全的重要性
  > - 政务、商务、金融、军事等

- [x] 网络安全是一个跨多门学科的综合性科学
  > - 包括：通信技术、网络技术、计算机软件、硬件设计技术、应用密码学、密码学数学基础等
  > - 在理论上，网络安全是建立在 `密码学以及协议设计` 的基础上的
  > - 从技术上，网络安全取决于两个方面：网络设备的硬件和软件的安全，以及设备的访问控制

### 常见的不安全因素

- [x] 物理因素：设备在物理防护上不安全，电磁波泄漏等

- [x] 系统因素：系统软、硬件漏洞，病毒感染，漏洞入侵

- [x] `网络因素` ：网络协议流程漏洞，会话劫持，数据篡改，故意的网络拥塞，(分布式)拒绝服务

- [x] 管理因素：(管理员)安全意识淡漠，误操作

### 导致不安全的原因

- [x] `自身的缺陷` ： ***系统软硬件缺陷、网络协议的缺陷等***
- [x] `开放性`
  > - **系统开放** ：计算机及计算机通信系统是根据行业标准规定的接口建立起来的。
  > - **标准开放** ：网络运行的各层协议是开放的，并且标准的制定也是开放的。
  > - **业务开放**：用户可以根据需要开发新的业务。
- [x] `黑客攻击`
  > - **基于兴趣的入侵 (传统意义上的Hacker)**
  > - **基于利益的入侵**
  > - **国与国、企业与企业之间的信息战**

### 六大网络安全的特征

- [x] `机密性Confidentiality` 信息不泄漏给非授权的用户、实体或者过程的特性。

- [x] `完整性Integrity`  数据未经授权不能进行改变的特性，即信息在存储或传输过程中保持不被修改、不被破坏的特性

- [x] `可用性Availability` 可被授权实体访问并按需求使用的特性，即当需要时应能存取所需的信息，也包括引入的安全功能不能明显影响用户对服务的使用

- [x] `可认证性Authenticity` 与完整性存在关联，要求数据来自所声称的实体，或者合法用户

- [x] `不可否认性Non-repudiation` 做过的行为和接受过的信息不能抵赖，该能力有时又被称为 `可审计性Accountability` ，要求可事后追溯，不可否认

- [x] `可控性Controllability`  对网络信息的传播及内容具有控制能力(也就是在信息发生冲突或者矛盾时，信息源可以各抒己见)

> 前三种特征是公认的( `CIA` )，后三个是根据不同教材有不同的说法。

### 常见攻击手段

- [x] `社会工程Social Engineering` 攻击者可通过各种社交渠道获得有关目标的结构、使用情况、安全防范措施等有用信息从而提高攻击成功率。

- [x] `口令破解password cracking` 攻击者可通过获取口令文件，然后运用口令破解工具获得口令，也可通过猜测或窃听等方式获取口令

- [x] `地址欺骗IP Spoofing` 攻击者可通过伪装成被信任的IP 地址，邮件地址等方式来骗取目标的信任

- [x] `会话劫持Session Hijacking` 在合法的通信连接建立后，攻击者通过阻塞或摧毁通信的一方来接管已经过认证建立起来的连接，从而假冒被接管方与对方通信

- [x] `网络窃听Network Eavesdropping` 网络的开放性使攻击者可通过直接或间接窃听获取所需信息

- [x] `数据篡改Data Tampering` 攻击者可通过截获并修改数据或重放数据等方式破坏数据的完整性

- [x] `恶意扫描Malicious scan` 攻击者可编制或使用现有扫描工具发现目标的漏洞，进而发起攻击

- [x] `基础设施破坏Infrastructure destruction` 攻击者可通过破坏DNS 或路由信息等基础设施，使目标陷于孤立

- [x] `数据驱动攻击Data-driven attack` 攻击者可通过施放病毒、特洛伊木马、数据炸弹等方式破坏或遥控远程目标

- [x] `拒绝服务Deny of Service` 攻击者可直接发动攻击，也可通过控制其它主机发起攻击，使目标瘫痪，如发送大量的数据洪流阻塞目标

#### 常见攻击小结

- [x] $\text{中断(Interruption)} \leftarrow \rightarrow \text{可用性(Availability)}$

- [x] $\text{窃听(Interception)} \leftarrow \rightarrow \text{机密性(Confidentiality)}$

- [x] $\text{修改(Modification)} \leftarrow \rightarrow \text{完整性(Integrity)}$

- [x] $\text{伪造(Fabrication)} \leftarrow \rightarrow \text{可认证性(Authenticity)}$

<p align="center">
  <img src="./img/常见攻击小结.png" alt="常见攻击小结">
  <p align="center">
   <span>常见攻击小结</span>
  </p>
</p>

### 信息安全分类

<p align="center">
  <img src="./img/信息安全分类.png" alt="信息安全分类">
  <p align="center">
   <span>信息安全分类</span>
  </p>
</p>

### 网络安全的主要任务

- [x] 保障网络与系统
  > - 安全、可靠、高效、可控、持续地运行和被访问

- [x] 保障信息
  > - 机密、完整、可认证、不可否认地传输和使用

### 需要保护的对象

- [x] 硬件
  > - 服务器、路由器、用户终端、物联网设备等

- [x] 软件
  > - 操作系统、应用软件等

- [x] 数据
  > - 电子商务、电子政务、电子邮件、信息发布、社交媒体等场景下的可能导致隐私泄露的敏感数据

## 1.2 网络参考模型与安全模型

- [x] 网络的体系结构
  > - 采用分层原则
  > - 分层、协议与接口的集合

- [x] 网络参考模型
  > - ISO - OSI (国际标准化组织-开放系统互连)模型
  > - TCP/IP模型(IETF)

- [x] 安全体系结构：ITU-T的X.800(ISO安全框架)和IETF的RFC2828
  > - 安全攻击 Security Attacks
  > - 安全机制 Security Mechanisms
  > - 安全服务 Security Services

- [x] 安全模型
  > - `网络安全模型Model for Network Security` : 涉及信息在网络传输中的安全(公网上的私有性保护)
  > - `网络访问安全模型Network Access Security Model` ：涉及网络或者系统本身的安全(访问控制)

### ISO-OSI模型

<p align="center">
  <img src="./img/ISO-OSI模型.png" alt="ISO-OSI模型">
  <p align="center">
   <span>ISO-OSI模型</span>
  </p>
</p>

- [x] 1. 物理层：缆线，信号的编码，网络接插件的电、机械接口

- [x] 2. 数据链路层：成帧，差错控制、流量控制，物理寻址，媒体访问控制

- [x] 3. 网络层：路由、转发，拥塞控制

- [x] 4. 传输层：为会话层提供与下面网络无关的可靠消息传送机制

- [x] 6. 表示层：在两个应用层之间的传输过程中负责数据的表示语法

- [x] 7. 应用层：处理应用进程之间所发送和接收的数据中包含的信息内容。

### 数据的封装

<p align="center">
  <img src="./img/数据的封装.png" alt="数据的封装">
  <p align="center">
   <span>数据的封装</span>
  </p>
</p>

### TCP/IP模型

<p align="center">
  <img src="./img/TCP-IP模型.png" alt="TCP/IP模型">
  <p align="center">
   <span>TCP/IP模型</span>
  </p>
</p>

### OSI与TCP/IP模型的比较

- [x] 相同点：
  > - 1. 都是基于独立的协议栈概念。
  > - 2. 两者都有功能相似的应用层、传输层、网络层。

- [x] 不同点：
  > - 1. 在OSI模型中，严格地定义了服务、接口、协议；在TCP/IP模型中，并没有严格区分服务、接口与协议。
  > - 2. OSI模型支持非连接和面向连接的网络层通信，但在传输层只支持面向连接的通信；TCP/IP模型只支持非连接的网络层通信，但在传输层有支持非连接和面向连接的两种协议可供用户选择。
  > - 3. TCP/IP模型中不区分、甚至不提起物理层和数据链路层。

### 安全体系结构

- [x] RFC 2828 (Internet Security Glossary)
- [x] X.800 (Security Architecture for OSI)
  > - `安全攻击Security Attacks` 损害机构所拥有信息的安全的任何行为
  > - `安全服务Security Services` 系统提供的对资源进行特殊保护的进程或者通信服务
  > - `安全机制Security Mechanisms` 设计用于检测、预防安全攻击或者恢复系统的机制
- [x] 用一种或多种 $\underline{安全机制}$ 来实现 $\underline{安全服务}$ ， $\underline{安全服务}$ 致力于抵御 $\underline{安全攻击}$ 。

### 安全体系结构————安全攻击

- [x] `主动攻击(active attack)` : 更改数据流, 或伪造假的数据流。
  > - 伪装 Masquerade
  > - 重放Replay
  > - 篡改Modification
  > - 拒绝服务Denial of Service

<p align="center">
  <img src="./img/主动攻击.png" alt="主动攻击">
  <p align="center">
   <span>主动攻击</span>
  </p>
</p>

- [x] 被动攻击(passive attack): 对传输进行偷听与监视, 获得传输信息, 但不对通信和数据做任何修改。
  > = 窃听攻击Eavesdrop
  > 流量分析Traffic analysis
  > 破解弱加密的数据流cracking of weakly-encrypted data streams

<p align="center">
  <img src="./img/被动攻击.png" alt="被动攻击">
  <p align="center">
   <span>被动攻击</span>
  </p>
</p>

## 1.3 网络各层的相关安全协议

## 1.4 密码学基础知识

## 1.5 数字签名与认证技术

## 1.6 网络安全的标准组织

# 第二章：公钥基础设施PKI  
# 第三章：IPSec-AH和ESP 
# 第四章：IPSec-IKE   
# 第五章：SSL/TLS协议  
# 第六章：防火墙与NAT
# 第七章：虚拟专用网VPN   
# 第八章：应用层安全协议  
# 第九章：无线局域网安全  
