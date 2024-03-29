# 课前须知

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
  > - 2. 两者都有功能相似的应用层、传输层、网络层(后者是前者的协议基础上总结出来的)。

- [x] 不同点：
  > - 1. 在OSI模型中，严格地定义了服务、接口、协议；在TCP/IP模型中，并没有严格区分服务、接口与协议。
  > - 2. OSI模型支持非连接和面向连接的网络层通信，但在传输层只支持面向连接的通信；TCP/IP模型只支持非连接的网络层通信，但在传输层有支持非连接和面向连接的两种协议可供用户选择。(对于电信ATM结构模型我国当前使用OSI模型，互联网一般都是TCP/IP模型，所以如果手机打电话由4G转为2G，也是因为语音通信为2G技术所以会回退)
  > - 3. TCP/IP模型中不区分、甚至不提起物理层和数据链路层。

### 安全体系结构

- [x] RFC 2828 (Internet Security Glossary)
- [x] X.800 (Security Architecture for OSI)
  > - `安全攻击Security Attacks` 损害机构所拥有信息的安全的任何行为
  > - `安全服务Security Services` 系统提供的对资源进行特殊保护的进程或者通信服务
  > - `安全机制Security Mechanisms` 设计用于检测、预防安全攻击或者恢复系统的机制
- [x] 用一种或多种 $\underline{安全机制}$ 来实现 $\underline{安全服务}$ ， $\underline{安全服务}$ 致力于抵御 $\underline{安全攻击}$ 。

### 安全体系结构————安全攻击

- [x] `主动攻击(active attack)` : 更改数据流, 或伪造假的数据流(相比被动攻击而言，主动攻击更容易被检测和监察)。
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

- [x] `被动攻击(passive attack)` : 对传输进行偷听与监视, 获得传输信息, 但不对通信和数据做任何修改(有时候可以通过某些方法，将被动攻击变为主动攻击，比如在量子信道中窃听攻击为主动攻击)。
  > - 窃听攻击Eavesdrop
  > - 流量分析Traffic analysis
  > - 破解弱加密的数据流cracking of weakly-encrypted data streams

<p align="center">
  <img src="./img/被动攻击.png" alt="被动攻击">
  <p align="center">
   <span>被动攻击</span>
  </p>
</p>

### 安全体系结构————安全机制

- [x] 特定的安全机制(8种)
  > - `加密Encipherment` 用加密算法对信息加密, 保护信息的机密性
  > - `数字签名Digital Signature` 用签名算法对信息进行计算, 计算结果附加于信息单元。用于身份认证、数据完整性和非否认服务
  > - `访问控制Access Control` 用于实施资源访问权限的机制
  > - `数据完整性Data Integrity` 用于确保信息的完整性
  > - `认证交换Authentication Exchange` 确保信息交换的实体是所声称的实体，通过信息交换以确保实体身份，包括公知密码、特征、位置信息等
  > - `流量填充Traffic Padding` 填充信息，防止流量分析
  > - `路由控制Route Control` 能够为特定数据选择特定基于路由的安全通道
  > - `公证Notarization` 采用可信任的第三方以确保一些信息交换的属性

- [x] 另外有其他5种普通的安全机制
  > - 可信功能Trusted Functionality、安全标记Security Label、事件检测Event Detection、安全审计跟踪Security Audit Trail、安全恢复Security Recovery。

### 安全体系结构————安全服务

<p align="center">
  <img src="./img/安全体系结构————安全服务.png" alt="安全体系结构————安全服务">
  <p align="center">
   <span>安全体系结构————安全服务</span>
  </p>
</p>

> 对等实体认证是指两个人回话之间彼此对对方的身份的认证，数据源认证是对信息来源单方确认

### 基本的安全设计准则

- [x] 主要准则
  > - 机制的经济性：安全机制设计简单和短小，便于测试和验证
  > - 故障安全默认：基于许可而不是排除
  > - 完整的监察：根据访问控制机制进行检查
  > - 开放的设计：安全机制的设计公开而不是保密
  > - 权限分离：多个权限属性来实现对首先资源的访问，例如，多因素用户认证
  > - 最小权限：每个进程或者使用者执行任务所需的最小权限集。例如，基于角色的访问控制
  > - 隔离、封装、分层、模块化

### 安全服务与攻击的关系

<p align="center">
  <img src="./img/安全服务与攻击的关系.png" alt="安全服务与攻击的关系">
  <p align="center">
   <span>安全服务与攻击的关系</span>
  </p>
</p>

### 安全服务与机制的关系

<p align="center">
  <img src="./img/安全服务与机制的关系.png" alt="安全服务与机制的关系">
  <p align="center">
   <span>安全服务与机制的关系</span>
  </p>
</p>

### 网络安全模型：实现端到端的安全通信

<p align="center">
  <img src="./img/网络安全模型.png" alt="网络安全模型">
  <p align="center">
   <span>网络安全模型</span>
  </p>
</p>

> - 数字信封：先对信息签名, 然后用对称密钥加密，再把对称密钥用收方公钥加密, 附在信息后。总之, 收方公钥加密两个收方会话的对称密钥
> - 端到端安全通信
> > - 可信第三方制定规则约束信息发送接收和传输
> > - 信息通过安全可靠的方式进行转化后传输
> > - 保证身份认证, 信息机密性, 完整性, 不可否认性
> > - 双向认证

### 网络访问安全模型：保护信息系统免遭恶意访问

<p align="center">
  <img src="./img/网络访问安全模型.png" alt="网络访问安全模型">
  <p align="center">
   <span>网络访问安全模型</span>
  </p>
</p>

> - 保护信息系统免遭恶意访问
> > - 防火墙和安全网关
> > - 入侵检测系统
> > - 虚拟专用网
> > - 保证可用性, 可控性
> > - 强调用户这端的认证，淡化基站和服务器端的认证

## 1.3 网络各层的相关安全协议

- [x] 链路层：链路隧道协议, 加密技术

- [x] 网络层：包过滤机制, NAT, IPSec协议, VPN

- [x] 传输层：SSL/TLS 协议

- [x] 应用层：HTTPS, PGP, S/MIME, DNSSEC等

<p align="center">
  <img src="./img/网络各层的相关安全协议2.png" alt="网络各层的相关安全协议">
  <p align="center">
   <span>网络各层的相关安全协议</span>
  </p>
</p>

<p align="center">
  <img src="./img/网络各层的相关安全协议3.png" alt="网络各层的相关安全协议">
  <p align="center">
   <span>网络各层的相关安全协议</span>
  </p>
</p>

## 1.4 密码学基础知识

### 1. 密码学分类

- [x] 按发展进程或体制分
  > -  `古典密码Classical Cipher` 基于字符替换的密码，现在已很少使用了，但是它代表了密码的起源
  > -  `对称密钥体制Symmetric-Key System` 加密密钥和解密密钥相同，这些算法也叫作单钥密码体制(one-key system)
  > -  `非对称密钥体制Asymmetric-Key System` 加密密钥和解密密钥不同，也叫公钥密码体制(public key system)或双钥密码体制(two-key system)

- [x] 按加密模式分
  > -  `序列密码Stream cipher` 序列密码 $\underline{按位或字节加密}$ , 也可以称为流密码, 序列密码是手工和机械密码时代的主流。
  > -  `分组密码block cipher` 分组密码将明文分成 $\underline{固定长度的组}$ , 用同一密钥和算法对每一块加密, 输出也是固定长度的密文。

### 2. 古典密码

- [x] DES(数据加密标准，Data Encryption Standard) 
  > - 背景
  > > - 1973年，NBS(后来的NIST, National Institute of Standards and Technology)美国国家标准局 `征集数据加密标准方案`
  > > - 1974年，IBM的Tuchman和Meyers发明Luciffer加密算法, NBS公布了IBM公司提供的该密码算法，以标准建议的形式在全国范围内征求意见
  > > - 1977年1月15日, DES正式颁布，供商业界和非国防性政府部门使用，同年7月15日生效
  > 
  > - DES是一种对二元数据进行加密的算法，数据分组长度为 `64位` ，密文分组长度也是 `64位` ，使用的密钥为 `64位` ，有效密钥长度为 `56位` ，有 `8位` 用于奇偶校验，解密时的过程和加密时相似，但密钥的顺序正好相反，DES的整个体制是公开的，系统的安全性完全靠密钥的保密。

<p align="center">
  <img src="./img/DES算法流程.png" alt="DES算法流程">
  <p align="center">
   <span>DES算法流程</span>
  </p>
</p>

<p align="center">
  <img src="./img/Single Round of DES Algorithm.png" alt="Single Round of DES Algorithm">
  <p align="center">
   <span>Single Round of DES Algorithm</span>
  </p>
</p>

#### DES算法的破解

- [x] DES使用了近 25年时间，它具有很强的抗密码分析能力，但它的密钥长度只有 $56比特$ ， $56-bit$ 密钥有 $2^{56} = 72,057,584,037,927,936 ≈ 7.2亿亿$ 之多，随着计算机运算能力的增加，56比特长度的密码系统显得不安全了。

- [x] 1997年，RSA公司发起破译RC4、RC5、MD2、MD5，以及DES的活动，破译DES奖励10000美金。
  > - 由Roche Verse牵头的工程小组动用了70000多台通过因特网连接起来的 计算机系统，花费了96天找到了密钥。
  > - 1998年7月，电子前沿基金会花费25万美圆制造的一台机器在不到3天的时间里攻破了DES。
  > - 1999年在超级计算机上只要22小时！

#### 对称密码的性能

- [x] 安全性能
  > - 密钥长度
  > - 分组长度
  > - 轮数
  > - 密钥编排函数
  > - 对密码分析的抵抗能力

- [x] 实现性能
  > - 计算开销
  > - 内存利用

#### 对加密系统的攻击

- [x] 未知算法攻击：算法未知，仅从密文进行破译

- [x] 仅知密文攻击(Ciphtext Only Attack，COA)：根据加解密算法和密文进行破译

- [x]  `已知明文攻击(Known Plaintext Attack，KPA)` ：攻击者拥有部分密文和对应的明文，根据算法寻找密钥

- [x]  `选择明文攻击(Chosen Plaintext Attack，CPA)` ：有选择地使用任意明文和与之对应的密文信息，根据算法寻找密钥

- [x]  `选择密文攻击(Chosen Ciphertext Attack，CCA)` ：具有CPA的能力之外，还可以有选择地使用密文和与之对应的明文信息，根据算法寻找密钥

#### 其他算法

- [x] 三重DES
  > - 使用三个密钥对数据块进行三次DES操作，三重DES有四种模型：
  > > - DES-EEE3 使用三个不同密钥顺序进行三次加密变换(实际上连续几次加密等效于用另一个密钥进行一次加密，所以实际上不用)
  > > - **DES-EDE3** 使用三个不同密钥依次进行加密-解密-加密变换 ( **3DES标准，兼容性考虑** )
  > > - DES-EEE2 其中密钥K1=K3 顺序进行三次加密变换
  > > - DES-EDE2 其中密钥K1=K3 依次进行加密-解密-加密变换

- [x] 3DES问题所在
  > - 算法开销
  > - 采用64bits分组长度

- [x] AES的出现
  > - 1997年NIST征集高级加密标准
  > > - 要求与3DES等同或者更高的安全强度，且效率显著提高。要求块长度为 `128位` ，密钥长度可以是 `128、192、256位`
  > 
  > -2001年，两轮评估，最终选择比利时密码学家提出的Rijndael算法，成为正式标准。

- [x] IDEA
  > - IDEA是国际数据加密算法(International Data Encryption Algorithm)的缩写，是1990年由瑞士联邦技术学院X.J.Lai(来学嘉)和Massey提出的建议标准算法，称作PES(Proposed Encryption Standard)，Lai 和Massey 在1992 年进行了改进，强化了抗差分分析的能力，改称为IDEA ，它也是对 `64bit` 大小的数据块加密的分组加密算法，密钥长度为 `128位` ，它基于“ `相异代数群上的混合运算` ”设计思想算法，用硬件和软件实现都很容易，它比DES在实现上快得多。
  > - 被推荐使用在 `PGP (Pretty Good Privacy)` 软件中
  > - 64位明文经128位密钥加密成64位密文，穷举分析需要 $10^{38}$ 次试探，按每秒100万次计算说，则需要 $10^{13}$ 年。
  > - 加密密钥与解密密钥不同，但是从一个主密钥派生出来，因此仍是对称的加密体制，目前尚无可验证的破译方法。算法本身倾向于软件实现，加密速度快。

- [x] Blowfish
  > - 1993年开发，密钥长度可变，最长可达448位，实际中常采用128位，块长度64

- [x] RC5
  > - 提出者：Ronald L. Rivest
  > - 1994年开发，可变轮数，可变长密钥
  > - 其后续版本RC6是作为AES的候选方案之一
  > -  `RC4是流密码算法` (密钥生成伪随机比特流，与明文按bit异或)

- [x] CAST-128
  > - 密钥长度40-128bits可变，每轮的函数互相不同，CAST-256提供更长的密钥长度

#### 几种对称加密算法的比较

<div align="center">
  <table>
  <thead>
    <tr>
      <th>算法</th>
      <th>密钥长度</th>
      <th>轮数</th>
      <th>数学计算</th>
      <th>应用</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>DES</td>
      <td>56</td>
      <td>16</td>
      <td>异或、固定S盒</td>
      <td>SET，Kerberos</td>
    </tr>
    <tr>
      <td>Triple DES</td>
      <td>112或168</td>
      <td>48</td>
      <td>异或、固定S盒</td>
      <td>PGP，S/MIME</td>
    </tr>
    <tr>
      <td>IDEA</td>
      <td>128</td>
      <td>8</td>
      <td>异或、加法、乘法</td>
      <td>PGP</td>
    </tr>
    <tr>
      <td>Blowfish</td>
      <td>可变至448</td>
      <td>16</td>
      <td>异或、变长S盒、加法</td>
      <td></td>
    </tr>
    <tr>
      <td>RC5</td>
      <td>可变至2048</td>
      <td>可变至255</td>
      <td>加法、减法、异或、旋转</td>
      <td></td>
    </tr>
    <tr>
      <td>CAST-128</td>
      <td>40至128</td>
      <td>16</td>
      <td>加法、减法、异或、旋转、固定S盒</td>
      <td>PGP</td>
    </tr>
  </tbody>
</table>
</div>

#### 分组密码的工作模式

- [x] 分组密码一次处理一个数据分组。

- [x] 对于较长的明文，在分解成若干个分组之后，采用相同的密钥进行加密，NIST定义了5种工作模式
  > - 电码本(ECB，Electronic Codebook)模式
  > - 密码分组链接(CBC，Cipher-block chaining)模式
  > - 密码反馈(CFB，Cipher feedback)模式
  > - 输出反馈(OFB，Output Feedback)模式
  > - 计数器(CRT， Counter)模式

##### 电码本(ECB, Electronic Codebook)模式

- [x] 直接应用密码算法的工作模式

- [x] 给定明文 $x=x_1x_2 \dots$ ,将它分为 $b$ 比特长的 $x_i$ ， $e_k$ 是加密算法，产生密文分组 $c_i = e_k(x_i)$ ，完整的密文 $c$ 按次序将 $c_i$ 连接起来：即 $c= c_1 c_2 \dots$ 。

- [x] 解密为 $x_i=d_k(c_i)$

- [x] **存在明显缺点：相同的明文加密后得到的密文是相同的** 。

<p align="center">
  <img src="./img/ECB加密.png" alt="ECB加密">
  <p align="center">
   <span>ECB加密</span>
  </p>
</p>

<p align="center">
  <img src="./img/ECB解密.png" alt="ECB解密">
  <p align="center">
   <span>ECB解密</span>
  </p>
</p>

##### 密码分组链接(CBC, Cipher-block chaining)模式

- [x] 给定明文的一个比特串 $x=x_1x_2 \dots$,  $x_i$ 是 $b$ 比特分组， $IV$ 是一个初始向量。
  > - $c_1 = e_k (x_1⊕IV)$ ，
  > - $c_2 = e_k (x_2⊕c_1)$ ，
  > - $c_i = e_k (x_i⊕c_{i-1})$

- [x] 解密：
	> - $x_1 = d_k (c_1)⊕IV$
	> - $x_i = d_k (c_i)⊕c_{i-1}$

<p align="center">
  <img src="./img/CBC加解密.png" alt="CBC加解密">
  <p align="center">
   <span>CBC加解密</span>
  </p>
</p>

> 当解密时某一密文分组出现错误，只会影响当前分组和下一分组的解密；而加密时，明文分组出错会影响当前分组和后续所有分组的加密，但是接收方解密时会正确解密，得到的明文除了出错的一组都是正确的。

##### 密码反馈(CFB, Cipher FeedBack)模式

- [x] 给定明文的一个比特串 $x=x_1x_2 \dots$ ,  $x_i$ 是 $s$ 比特分组， $IV$ 是一个初始向量。
  > - $z_1 = e_k (IV)$ ， $c_1 = x_1⊕z_1$ 的 $s$ 位
  > - $z_2 = e_k (IV 移位||c_1的s位)$ ， $c_2 = x_2⊕z_2$ 的 $s$ 位
  > - $z_i = e_k (上个移位寄存器内容移位||ci-1 的s位)$ ， $c_i= x_i⊕z_i$ 的 $s$ 位

- [x] 解密：
	> - $z_1 = e_k (IV)$ ， $x_1 = c_1⊕z_1$ 的 $s$ 位
	> - $z_i = e_k (上个移位寄存器内容移位||ci-1 的s位)$ ， $x_i= c_i⊕z_i$ 的 $s$ 位

<p align="center">
  <img src="./img/CFB加解密.png" alt="CFB加解密">
  <p align="center">
   <span>CFB加解密</span>
  </p>
</p>

<p align="center">
  <img src="./img/CFB加解密1.png" alt="CFB加解密">
  <p align="center">
   <span>CFB加解密</span>
  </p>
</p>

> 参考下面的图，上面那个并不太准确，也就是第一次加密时，移位寄存器中存储 $b$ 位(一般是64)的初始向量 $IV$ 先进行加密，然后舍弃后面的 $b-s$ 位，取最前 $s$ 位与明文分组加密得到密文，第二次加密也就是对移位寄存器中 $b$ 位的初始向量前移 $s$ 位(原来的前 $s$ 位)舍弃，将第一组密文放在最后 $s$ 位填充进去，补到 $b$ 位。依次重复即可，所以到 $\frac{b}{s}$ 次后加密，移位寄存器中的 $b$ 位也就不含初始向量的任何部分了。同理密文传输错误时，也最多影响后 $\frac{b}{s}$ 个分组。

##### 输出反馈(OFB, output-Feedback)模式

- [x] $z_1 = e_k (IV),c_1 = x_1⊕z_1$
- [x] $z_2 = e_k (z_1),c_2 = x_2⊕z_2$
- [x] $z_i = e_k (z_{i-1}),c_i = x_i⊕z_i$

- [x] 解密：
	> - $z_1 = e_k (IV),x_1 = c_1⊕z_1$
	> - $z_i = e_k (z_i),x_1 = c_1⊕z_1$

<p align="center">
  <img src="./img/OFB加解密.png" alt="OFB加解密">
  <p align="center">
   <span>OFB加解密</span>
  </p>
</p>

- [x] $z_1 ,…, z_i,…$ 可以提前计算

##### 计数器(CRT, CounTeR)模式

- [x] 给定计算器初始值 `counter`
  > - $z_1 = e_k (counter),c_1 = x_1⊕z_1$
  > - $z_2 = e_k (counter+1),c_2 = x_2⊕z_2$
  > - $z_i = e_k (counter+i-1),c_i = x_i⊕z_i$

- [x] 解密：
	> - $z_i = e_k (counter+i-1),x_i = c_i⊕z_i$

<p align="center">
  <img src="./img/CRT加解密.png" alt="CRT加解密">
  <p align="center">
   <span>CRT加解密</span>
  </p>
</p>

### 3. 公开密钥算法

- [x] 对称密码算法问题：
  > - 密钥管理量问题：潜在通信的两两分别用一对密钥，当用户量增大时，密钥空间急剧增大。
  > - 对称算法无法实现抗否认需求——数字签名

- [x] 非对称密码体制的基本原则
  > - 加密能力与解密能力是分开的
  > - 密钥分发简单
  > - 需要保存的密钥量大大减少，N个用户只需要N个，除了个人私钥之外，公钥均可以公开保存
  > - 可满足不相识的人之间保密通信
  > - 可以实现数字签名

<p align="center">
  <img src="./img/公开密钥算法加密.png" alt="公开密钥算法加密">
  <p align="center">
   <span>公开密钥算法加密</span>
  </p>
</p>

<p align="center">
  <img src="./img/公开密钥算法认证.png" alt="公开密钥算法认证">
  <p align="center">
   <span>公开密钥算法认证</span>
  </p>
</p>

#### 公开密钥算法基本思想

- [x] 公钥密码又称为双钥密码和非对称密码，1976年由Diffie和Hellman在其邀搞论文“密码学新方向”（ New Directions in Cryptography ）一文中提出的。(2016年图灵奖)

- [x] RSA是1978年MIT的Rivist, Shamir 和Adlemar开发的第一个公钥密码体制，最早提出的满足要求的公钥算法之一。(2002年图灵奖)

#### RSA密码体制基本原理

- [x] A. 密钥的生成
  > - 选择 $p, q$ ， $p, q$ 为互异素数，计算 $n=p×q$ , $φ(n)=(p-1)(q-1)$ , 选择整数 $e$ 与 $φ(n)$ 互素，即 $gcd(φ(n),e)=1,1<e<φ(n)$ 计算 $d$ ,使 $d=e^{-1}(modφ (n))$ ,公钥 $Pk=\lbrace e, n\rbrace$ ; 私钥 $Sk=\lbrace d, n\rbrace$

- [x] B. 加密 (用 $e, n$ )，
  > - 明文是以分组方式加密的，每一个分组的比特数应小于n的二进制表示，即每一个分组的长度应小于 $\log _2n$
  > - 明文 $M<n$ ， 密文 $C=M^e(mod n)$ .

- [x] C. 解密 (用 $d, n$ )
  > - 密文C， 明文 $M=C^d (mod n)$

##### RSA的安全分析

- [x] 选取的素数 $p, q$ 要足够大，使得给定了它们的乘积 $n$ , 在不知道 $p, q$ 情况下分解 $n$ 在计算上是不可行的。

- [x] 1999年, 一个292台计算机组成的网络花了5.2个月时间分解了一个155位的十进制数 (512比特)。基于短期安全性考虑, 要求n的长度至少应为1024比特, 而长期安全性则需n至少为2048比特。

#### 其它公钥算法

- [x] ELGamal密码
  > - 1985年ELGamal设计的密码算法，该算法是基于有限域上离散对数问题求解的困难性。

- [x] 椭圆曲线密码
  > - 1985年N. Koblitz和V. Miller分别独立提出了椭圆曲线密码体制(ECC), 其依据就是定义在椭圆曲线点群上的离散对数问题的难解性。

- [x] Diffie-Hellman密钥交换

### 4. Diffie-Hellman密钥交换(DH密钥交换)

<p align="center">
  <img src="./img/DH密钥交换.png" alt="DH密钥交换">
  <p align="center">
   <span>DH密钥交换</span>
  </p>
</p>

> - 考研常考或者期末常考。
> - $g$ 称为本原根， $K=(g^{X_A})^{X_B}=(g^{X_B})^{X_A} mod \ B$ 。

- [x] 防止中间人攻击
  > - 1. 数字签名，对自己的Y用自己的私钥签名，但是这个不常用，这个可能导致公私钥被窃取重用；
  >   2. HMAC\用户认证：A向B发一个随机数，B对随机数用私钥签名，然后发给A，或者用公钥加密，发给A。A进行验证即可，但是有可能被中间人向B发起验证，在中间截取随机数，然后让B证明自己是B，B对随机数签名后重用这个数据此时可以冒充B，这个时候可以采用对随机数特殊定义的方法进行处理。
  >   3. 双向验证，这个也防不了重用。

## 1.5 数字签名与认证技术

- [x] 通信中潜在的威胁
  > - 消息伪造
  > - 内容篡改(如何判断有没有篡改:对明文添加校验位，校验位是明文的哈希对应，但是实际上都是用HMAC做)
  > - 延迟或重播
  > - 否认
 
- [x] 数字签名————消息的不可否认性

- [x] 消息认证————消息的完整性(不能提供消息的不可否认性)

### 1. 数字签名

- [x] 公钥密码学的一个重要应用就是数字签名，数字签名就是利用私钥生成签名，而用公钥验证签名。

- [x] 一个数字签名方案时是由签名算法和验证算法组成
  > - 签名算法利用私钥生成签名，称消息 $m$ 的签名为 $sig(m)$ ，然后将 $(m，sig(m))$ 发给接收方
  > - 验证算法利用签名者的公钥对 $sig(m)$ 进行解密，如果解密输出与 $m$ 一致，则为合法数据。

> - **对于大文件传输的签名，如果对整个文件签名，则有三个巨大开销，也就是源端签名的开销，传输巨大密文还有明文（这个是用于对端解密后比对的）的开销，验证端(目的端)的解密和对比的开销。所以实际应用中，对文件进行一个哈希，对比特数进行减少，再进行签名，对端只用对明文也进行哈希，对传输过来的签名后的密文进行公钥解密，比对就可以。这个时候开销就很小。实际上不管是不是大文件，只要是签名的，都是这么做的，开销小了两个数量级左右。**

- [x] 由于无法识别数字签名与其拷贝之间的差异，所以，在数字签名前应加上时间戳。

- [x] 数字签名标准(DSS)
  > - DSA(数字签名算法，是Elgamal公钥算法的一种变体)
  > - RSA

### 2. 消息认证

- [x] 提供数据源认证能力

- [x] 可用来做消息认证的函数有三类(合计4种方法)
  > - 直接用加密函数(通常不这么用)
  > > -  `用对称密钥加密` ，信息的一致作为对信息的认证
  > > -  `用公钥密码中的私钥加密` ，但加密速度太慢，实际使用时结合散列函数构成实用化的签名。
  > 
  > -  消息认证码MAC (Message Authentication Code)
	> > - 是对信源消息的一个编码函数, 以消息和密钥作为输入，定长输出，
	> - 散列函数 (Hash Function)+签名
	> > - 是一个公开的函数它将任意长的信息映射成一个固定长度的信息，需要结合公钥签名一起使用。

> - 开销： $非对称 >> 对称 >> 哈希 >> 异或$
> - 非对称协议一般情况： $协商参数 \rightarrow 非对称加密 \rightarrow DH交换密钥 \rightarrow 建立安全通道$

#### 消息认证码MAC

- [x] 利用函数 $f$ 和密钥 $k$ , 对要发送的明文 $x$ 或密文 $y$ 变换成 $r \ bit$ 的消息认证码 $f(k,x)$ (或 $f(k,y)$ ), 将其称为认证符附加在 $x$ (或 $y$ )之后发出, 接收者收到发送的消息序列后，按发方同样的方法对接收的数据(或解密后)进行计算, 应得到相应的 $r \ bit$ 数据

<p align="center">
  <img src="./img/消息认证码MAC.png" alt="消息认证码MAC">
  <p align="center">
   <span>消息认证码MAC</span>
  </p>
</p>

> - HMAC就是先哈希后MAC的协议

#### 散列函数

- [x] 单向散列函数(hash，杂凑函数)可以从一段很长的报文中计算出一个固定长度的比特串，这种散列函数通常称为报文摘要(message digest)，用于消息的完整性检验。

- [x] 单向散列函数H有以下特性：
  > 1. $H$ 能够应用于任何大小的数据块
  > 2. $H$ 产生固定长度的输出
  > 3. 对于任意给定的数据 $X$ ，易于计算 $H(X)$
  > 4. 对于任何给定的数据 $h$ ，计算 $H(X)=h$ 是不可行的
  > 5. 对于任意给定的数据 $X$ ，寻找满足 $H(Y)=H(X),Y≠X$ ,在计算上是不可行的。这也称为 <kbd>弱碰撞抵抗</kbd> 
  > 6. 寻找满足 $H(Y)=H(X)的(X,Y)$ 对，在计算上是不可行的。这也称为 <kbd>强碰撞抵抗</kbd>

- [x] **满足前5个性质的hash函数称为弱hash函数，如果6条都满足就称为强hash函数。**

- [x] 标准： `MD5` ( <kbd>128比特</kbd> )， `SHA-1` ( <kbd>160比特</kbd> )， `SHA-2` (包括6种)

> - ~~"派生"也就是从一个密钥发展多个，"拓展"就是多个变一个~~

##### 采用散列函数认证消息

<p align="center">
  <img src="./img/采用散列函数认证消息.png" alt="采用散列函数认证消息">
  <p align="center">
   <span>采用散列函数认证消息</span>
  </p>
</p>

> - 第一个不常用

## 1.6 网络安全的标准组织

- [x] 国际组织
  > - 国际标准化组织（ISO）
  > - 国际电信联盟（ITU-T）
  > - 国际电工委员会（IEC）
  > - 互联网协会 (ISOC)
  > > - 因特网工程任务组 (IETF)
  > > - 互联网研究任务组 (IRTF)
  > 
  > - 欧洲计算机制造商协会（ECMA）
  > - 美国国家标准技术研究所(NIST)
  > - 美国国家计算机安全中心（NCSC）
  > - 美国国防部（DOD） 

- [x] 国内组织
  > - 信息技术安全标准化委员会（CITS）
  > - 通信标准化协会 (CCSA)-TC260 全国信息安全标准化技术委员会

# 第二章：公钥基础设施PKI 

## 2.1 PKI基本概念

- [x] 什么是PKI呢？
	> - 公钥基础设施(Public Key Infrastructure, PKI)
	> - PKI是一个用 `非对称密码算法原理和技术` 来实现并提供安全服务的具有通用性的 `安全基础设施` 。是一种遵循标准的利用公钥加密技术为电子商务的开展提供安全基础平台的 `技术和规范` 。能够为所有网络应用提供采用加密和数字签名等密码服务所需要的 `密钥和证书管理` 。

- [x] 为什么需要PKI？
	> - 对可信第三方的需要(Certificate Authority, CA)
	> - 电子政务、电子商务对信息传输的安全需求， `统一标准`
	> - 在收发双方建立信任关系，提供身份认证、数字签名、加密等安全服务
	> - 收发双方不需要事先共享密钥，通过公钥加密传输会话密钥

- [x] 如何在通信双⽅间协商⼀个会话密钥
	> - 基于对称加密：通过选择⼀个密钥分发中⼼，为通信双⽅提供⼀个会话密钥。如 `Kerberos认证协议`
	> - 基于⾮对称加密：包括 `Diffie-Hellman密钥交换` ， `数字信封`

- [x] 什么是随机数？基于已学课程⼤致描述随机数的作⽤？
	> - 随机数是⼀种统计上独⽴且⽆偏的⼆进制数字序列
	> - 随机数作用:
	> > - 作为分组密码技术中的密钥
	> > - 作为流密码技术中的密钥或密钥流
	> > - ⽤于产⽣公钥密钥算法中的⼤素数、私钥等，如RSA中p和q的选取
	> > - ⽤于认证协议中防⽌重放攻击

- [x] 非对称密码体制(很多考试都有，还有小测)

<p align="center">
  <img src="./img/非对称密码体制.png" alt="非对称密码体制">
  <p align="center">
   <span>非对称密码体制</span>
  </p>
</p>

### 证书的基本结构(最简构成)(很多考试都有，还有小测)

- [x] ***通过可信CA的签名实现主体身份和主体公钥之间的绑定关系***
	> - 此时假设了 $CA$ 可信，这个是前提。

<p align="center">
  <img src="./img/证书的基本结构.png" alt="证书的基本结构">
  <p align="center">
   <span>证书的基本结构</span>
  </p>
</p>

> - 公钥证书由公钥、公钥所有者的主体身份信息、可信第三⽅的签名这样的整个数据块组成。

### PKI的组成

<p align="center">
  <img src="./img/PKI的组成.png" alt="PKI的组成">
  <p align="center">
   <span>PKI的组成</span>
  </p>
</p> 

- [x]  `认证中心CA(Certificate Authority)` 证书的签发机构，它是PKI的 `核心构件` ，是PKI应用中权威的、可信任的、公正的第三方机构。

- [x]  `注册机构RA(Registration Authority)` 注册功能也可以由CA直接实现，但随着用户的增加，多个RA可以分担CA的功能，作为CA的延展，可以 `增强可扩展性` 。按照特定的政策和管理规范对用户的资格进行审查，并执行是否同意给该申请人发放证书。撤销证书等操作，应注意的是 `RA不容许直接颁发证书或CRL` ~~(因为涉及到签名，类似 `RA` 没有签名私钥)~~ 。

- [x]  `证书库(Certification Library)` CA颁发证书和 `证书撤销列表CRL` 的集中存放地，提供公众查询，常用目录服务器提供服务，采用 `LDAP(Lightweight Directory Access Protocol)` 目录访问协议。
	> - 得到与之通信的实体的公钥，在证书中
	> - 验证通信实体的证书是否在CRL中，也基于签名

- [x]  `密钥备份及恢复系统`
	> -  `签名密钥对` ：签名私钥相当于日常生活中的印章效力，为保证其唯一性、抗否认性， `签名私钥不作备份` 。签名密钥的生命期较长。
	> -  `加密密钥对` ：加密密钥通常用于分发会话密钥，为防止密钥丢失时无法解密数据， `解密密钥应进行备份` 。这种密钥应频繁更换。

- [x]  `证书作废处理系统` 证书由于某种原因需要作废, 终止使用, 这将通过 `证书作废列表` (CRL, Certificate Revocation List)来完成, 证书撤销列表作为文件结构，也需要由CA进行签发。

- [x]  `自动密钥更新` 无需用户干预, 当证书失效日期到来时, 启动更新过程, 生成新的证书

- [x]  `密钥历史档案`  由于密钥更新，每个用户都会拥有多个旧证书和至少一个当前证书, 这一系列证书及相应私钥（除签名私钥）组成密钥历史档案。
	> - 避免他人抵赖，若旧的证书失效被放入黑名单或者销毁，可以抵赖旧证书的使用行为。

- [x]  `PKI应用接口系统` 是为各种各样的应用提供安全、一致、可信任的方式与PKI交互, 确保所建立起来的网络环境安全可信,并降低管理成本。

- [x]  `交叉认证` 多个PKI独立地运行, 相互之间应建立信任关系
	> - 多个PKI独立运行相互建立信任关系
	> - 两个CA间互相认证颁发证书

### 建立标准化PKI体系的主要优势

- [ ] 节省费用

- [ ] 互操作性

- [ ] 开放性

- [ ] 一致的解决方案

- [ ] 可验证性

- [ ] 可选择性

### PKI基本服务

- [x]  `认证`
	> - **实体鉴别, 数据来源鉴别** ~~(前者是认证实体身份，后者是认证数据最初源头，也就是不管转发者是谁，只关心最初的来源)~~

- [x]  `完整性`
	> - **哈希+数字签名技术, 消息认证码(数字信封传输对称密钥)**
 
- [x]  `保密性`
	> - **采用数字信封, 传输会话密钥**

- [x]  `不可否认性服务`
	> - **收据(receipt)的数字签名**
	> - **安全时间戳**

- [x]  `公证服务`
	> - **由CA充当第三方进行数据验证**

## 2.2 PKI和电子商务中常用的密码技术

### 信息加密/解密

#### PKI提供的安全手段与传统方法的比较

<p align="center">
  <img src="./img/PKI提供的安全手段与传统方法的比较.png" alt="PKI提供的安全手段与传统方法的比较">
  <p align="center">
   <span>PKI提供的安全手段与传统方法的比较</span>
  </p>
</p> 

#### 信息加密/解密

<p align="center">
  <img src="./img/信息加密-解密.png" alt="信息加密/解密">
  <p align="center">
   <span>信息加密/解密</span>
  </p>
</p> 

> - 由于非对称密码的运算复杂、加/解密速度慢, 因此信息的加密采用对称密码算法, 其会话密钥的分发采用非对称密码算法, 即  **采用 `收方的公钥` 对随机产生的会话密钥进行加密(称为 `数字信封` )** ( **可能会考15字以内说明数字信封** )。

> 注：这里是对 <kbd>随机产生的会话密钥</kbd> 进行加密，需要表述清楚，而非对 `随机数` 或 `会话密钥` 加密。

### 数字签名

- [x] 数字签名: 对待发的数据首先基于 `Hash` 生成一段 `数据摘要` ，再采用 `己方私钥` 基于非对称加密算法进行加密，结果 `附在原文上` 一起发送，接收方对其进行验证，判断原文真伪。从计算开销的角度，这种数字签名方法适用于对大文件的处理。

- [x] 数字签名在PKI中提供 `数据完整性保护` 和提供 `不可否认性服务` 。

> 注：在考虑源端加密和签名(或进行 `HMAC` )的顺序时，会考虑开支，在本课程中这个顺序一般是一样的，只有一个特例，所以这两个场景(不同顺序的两个场景)考试的时候必会考一个。
> > 一般采取先采取加密，再进行 `HMAC` ( `(E(M),sign)` ,反之为 `sign(E(M))` )，因为此时目的端可以通过 `HMAC` 可以知道该消息是否正确，若错误就可以不进行解密，可以进行省略解密步骤(这个建立在加密和 `HMAC` 的开销一致的情况，或加解密的开销小于验证或进行 `HMAC` 的情况)。
> >
> > 经常性的/频繁触发/周期性的情况，是需要优化的。

#### 具有数据摘要的数字签名

<p align="center">
  <img src="./img/具有数据摘要的数字签名.png" alt="具有数据摘要的数字签名">
  <p align="center">
   <span>具有数据摘要的数字签名</span>
  </p>
</p> 

### 报文检验码

- [x]  `报文检验码` , 也称消息认证码,  `MAC(Message Authentication Code)` ，是一种需要密钥(称为完整性密钥)参与的单向哈希函数, 采用这种方法也可以实现 `数据完整性服务` 。

### 数字信封(重点)

- [x] 信息发送端采用 <strong><kbd>接收端的公钥</kbd></strong> ，将一个通信密钥（即对称加密使用的对称密钥）就行加密，生成一个 <strong><kbd>数字信封</kbd></strong> 。

- [x] 接收端用 <strong><kbd>己方私钥</kbd></strong> 对数字信封进行解密操作, 获取该 <strong><kbd>对称密钥</kbd></strong> , 用它来解密收到的基于对称加密的加密信息。

#### 数字信封的使用示例————发送方

<p align="center">
  <img src="./img/数字信封的使用示例-发送方.png" alt="数字信封的使用示例-发送方">
  <p align="center">
   <span>数字信封的使用示例-发送方</span>
  </p>
</p> 

> - (1) 将要 ***传输的信息进行 `hash` 操作*** 后，得到一个数据摘要 `MD` ， $MD=hash(信息)$
> - (2) 发送者 $A$ 用自己的 ***私钥 `PVA` 对数据摘要 `MD` 进行加密*** ，得到 $A$ 的数字签名 `DS`
> - (3) 发送者 $A$ 将信息明文、数字签名和它的证书上的公钥三项信息，通过对称算法，用 ***对称密钥 `SK` 进行加密*** ，得密文 `E` ( **根据上述的说法，考虑实际开销时，其实应该先加密再签名这个位置是有问题的** )
> - (4) 发送者在发送信息之前，必须事先得到接受方 $B$ 的证书公钥 `PBB` ，用 ***`PBB` 加密 `SK` ，形成一个数字信封 `DE`***
> - (5) $E+DE+CertA$ 就是将密文与数字信封连接起来，并可选地附带证书，既A所发送的内容

> **注：公钥为 `PU` ，私钥为 `PR`** 。

#### 数字信封的使用————接收方

<p align="center">
  <img src="./img/数字信封的使用-接收方.png" alt="数字信封的使用-接收方">
  <p align="center">
   <span>数字信封的使用-接收方</span>
  </p>
</p> 

> - (1) 接收者 $B$ 用自己的私钥 `PVB` 解密数字信封 `DE` , 获取对称加密密钥 `SK`
> - (2) 接收者 $B$ 用 `SK` 将密文 `E` 解密还原成信息明文、数字签名 `DS` 和 $A$ 的证书公钥 `PBA`
> - (3) 证书验证, 获得 `PBA`
> - (4) $B$ 将数字签名用 $A$ 的公钥 `PBA` 进行解密, 得到信息摘要 `MD`
> - (5) $B$ 再将已收到的信息明文, 用同样的 `hash` 函数计算, 得到信息摘要 `MD'`
> - (6) 比较 `MD` 与 `MD'` , 若相等, 则接收。

### 双重数字签名(在SET协议中讲述)

## 2.3 PKI功能操作

### PKI功能操作概述

- [x] **PKI的运行操作主要经过六个步骤：**
	> - 1. 端实体向证书机构(CA)提出数字证书申请；
	> - 2. CA验明端实体身份，并 `签发数字证书` ；
	> - 3.  `CA将证书公布到证书库` 中；
	> - 4. 假设为电子邮件应用，端实体对电子邮件数字签名作为发送认证，确保邮件完整性，不可否认性，并发送给接收方。
	> - 5. 接收方接收邮件，首先获得证书，到证书库查明端实体证书的状态和有效性(在线)，证书库返回证书检查结果( `CRL检查` 等)，验证证书和公钥的绑定关系；
	> - 6. 用端实体的 `公钥验证数字签名(离线)` 。

<p align="center">
  <img src="./img/PKI的运行操作主要经过六个步骤.png" alt="PKI的运行操作主要经过六个步骤">
  <p align="center">
   <span>PKI的运行操作主要经过六个步骤</span>
  </p>
</p> 

### 证书的初始化、使用和撤销

<p align="center">
  <img src="./img/证书的初始化、使用和撤销.png" alt="证书的初始化、使用和撤销">
  <p align="center">
   <span>证书的初始化、使用和撤销</span>
  </p>
</p> 

#### 初始化阶段

- [x]  `初始化阶段` ：在终端实体能够使用PKI支持的服务之前，它们必须初始化以进入PKI。初始化由以下几步组成：
	> - `终端实体注册`
	> - **`密钥对产生`**
	> - **`证书创建`**
	> - `证书分发`
	> - `密钥备份`

<p align="center">
  <img src="./img/证书的初始化.png" alt="证书的初始化">
  <p align="center">
   <span>证书的初始化</span>
  </p>
</p> 

> - **注：用户的公私密钥对的产生有三种方式，视策略而定：**
> > - **用户自己产生密钥对**
> > - **CA为用户产生密钥对**
> > - **CA之外的其他可信第三方产生密钥对**

##### 证书创建 

<p align="center">
  <img src="./img/证书创建.png" alt="证书创建">
  <p align="center">
   <span>证书创建</span>
  </p>
</p> 

#### 使用阶段

- [x]  `使用阶段` ：一旦私钥和公钥证书已经产生并适当地分发，密钥/证书生命周期管理的颁发阶段即开始。这个阶段包括：
	> - `证书获取`
	> - `证书验证` ————确定一个证书的有效性
	> - 密钥恢复————对终端用户因为某种原因而丢失的 `加密密钥可` 以恢复，从CA或信任第三方处恢复。
	> - 密钥更新————当一个合法的密钥对将过期时，进行新的公/私钥的自动产生和相应证书的颁发

> - **证书获取的方式：**
> > - **发送者发送签名时，附加发送自己的证书**
> > - **单独发送证书**
> > - **从访问发布证书的目录服务器获得**
> > - **从其他公共站点的共享位置获得**

> - **验证证书的过程**
> > - **验证证书上的签名**
> > - **检查公钥证书是否已被撤销**
> > - **检查证书中所有的字段**

> 公钥是由CA提供或保存，但是私钥的一般保存在本地，一般采用加密存储的形式，由自己的 `Password` 加一个随机数的进行哈希加密存储，便于恢复。

##### 证书的签名验证过程

<p align="center">
  <img src="./img/证书的签名验证过程.png" alt="证书的签名验证过程">
  <p align="center">
   <span>证书的签名验证过程</span>
  </p>
</p> 

##### 证书验证

- [x]  `拆封证书`
	> - 目的：一个证书的“ `拆封` ”是为了从中获得一个公钥，可表示为X1P.X1《X2》。如果用可信任的CA的公钥可以“拆封”（验证）一个用户的证书，那么这个证书是该CA签发的。

- [x]  `证书链的认证(直到信任锚点)` ( `信任锚点` 也就是指自己信任的 `CA` 机构(可信第三方)，假设A不相信当前的 `CA` 机构B，但是B的验证是由 `CA` 机构C签发的，而C正好为A信任的 `CA` 机构，那么C为信任锚点)
	> - 所谓证书链的认证是想通过证书链追溯到可信赖的 `CA` 的根(信任锚点)，确认公钥的有效性和可信性。

> - 证书链(Certificate Chain)是一系列数字证书的集合，其中每个证书都由下一个证书签名，直到达到最终的根证书。证书链的目的是建立信任路径，验证数字证书的有效性。
> - 通常，证书链包括以下几个部分：
> - 1. **服务器证书（或端点证书）**：服务器证书是数字证书链的起点，用于验证服务器的身份。它包含了服务器的公钥、组织信息以及数字签名等内容。
> - 2. **中间证书（Intermediate Certificate）**：中间证书由受信任的证书颁发机构（CA）签发，用于将服务器证书与根证书相连接。如果服务器证书是由受信任的 CA 签发的，那么中间证书就是该 CA 的根证书。
> - 3. **根证书（Root Certificate）**：根证书是数字证书链的最后一个证书，它是信任的根源。根证书由操作系统或浏览器内置，用于验证中间证书的有效性。
> - 在验证证书链时，客户端会逐级验证每个证书的签名，确保每个证书都是由上一个证书签发的，直到到达根证书。如果证书链中的每个证书都可以成功验证，并且根证书被客户端信任，则客户端将信任服务器证书，建立安全连接。如果任何一个证书验证失败，或者根证书不被客户端信任，连接就会失败，因为无法建立信任路径。

- [x]  `证书撤销列表查询`
	> - 黑名单查询”，向证书库查询 `证书撤销列表`

- [x]  `字段验证`
	> -  `序列号验证`
	> > - 检查证书中签名实体序列号是否与签发者证书的序列号一致。
	>   
	> -  `有效期验证`
	> > - 检查日期是否有效、合法：
	> > > - 1. 用户证书的有效期和私钥有效期是否在CA证书的有效期内。否则交易是不安全的。
	> > > - 2. 用户证书的有效期中的起始时间应在CA证书的私钥有效期内。否则证书是不安全的。
	> 	
	> - 证书使用策略的认证
	> - ……

#### 撤销阶段

- [x] 撤销阶段：密钥/证书生命周期管理以撤销阶段来结束。此阶段包括如下内容：
	> - 证书过期————证书生命周期的自然结束
	> - 证书撤销————证书在过期之前被撤销。比如私钥泄露、关系终止 ~~(也就是解除和CA的证书关系，换一个CA)~~ 、CA签名私钥泄露或者变更等(以上两个阶段是不需要归档的)
	> - 存档(归档)————维持一个CRL和有关历史证书的记录(一般是关于终端实体的)，以便被过期的密钥资料所加密的数据能够被解密
	> - 审计信息————出于对密钥历史恢复、审计和解决争议的考虑所进行的密钥资料的安全第三方长期储存(写入存储后不可更改)

> - **CA应维护与安全有关的审计信息，如：**
> > - **产生密钥对**
> > - **证书的请求**
> > - **密钥泄露的报告**
> > - **证书中包括的某种关系的终止等**
> > - **证书使用过程**

##### CRL格式和生成方式

<p align="center">
  <img src="./img/CRL格式和生成方式.png" alt="CRL格式和生成方式">
  <p align="center">
   <span>CRL格式和生成方式</span>
  </p>
</p> 

##### 证书是否撤销的查询方式

- [x] 1. 在线查询：

<p align="center">
  <img src="./img/证书是否撤销的查询方式.png" alt="证书是否撤销的查询方式">
  <p align="center">
   <span>证书是否撤销的查询方式</span>
  </p>
</p> 

- [x] 2. 离线下载，本地查询（技术难点：如何更新）

##### 密钥/证书生命周期管理

<p align="center">
  <img src="./img/密钥-证书生命周期管理.png" alt="密钥/证书生命周期管理">
  <p align="center">
   <span>密钥/证书生命周期管理</span>
  </p>
</p> 

## 2.4 PKI体系的互通性与标准化

> 多用户验证对方 `CA` 证书的时候需要找到自己 `CA` 到对方 `CA` 的信任路径(跨域认证)，也就是需要知道对方 `CA` 是否可信，此时互通性和标准化就十分重要，同时信任度的体现在很多方面，比如推荐算法也是基于可信度的一种。

- [x] **信任关系**
	> - 建立全球统一的根CA( **显然不现实** ) 
	> -  `交叉认证` 方式：对等关系的CA互相签发(双向)
	> - 建立基于 `层次化结构` 信任路径(单向)
	> -  `分布式CA` (单向双向混合)

- [x] **信任的相关概念**
	> - 当一个安全个体看到另一个安全个体出示的证书时，他是否信任此证书？
	> -  `信任(Trust)`  :(Entity “A” trust entity “B” when “A” assumes that “B” will behave exactly as “A” expects.)如果一个实体假定另一个实体会严格的像它期望的那样行动，就称它 `信任` 那个实体.
	> - ` 可信CA` :如果一个个体假设CA能够建立并维持一个准确的“个体-公钥属性”之间的绑定，则他可以信任该CA，该CA为 `可信CA` 。

> - 信任假设模型有很多种:"诚实并好奇(用的比较多)(就是诚实给信息，但是不一定按照期望行动)"、"完全信任"、"半信任"。

### 信任CA结构

#### 层次模型

##### 严格的层次模型

<p align="center">
  <img src="./img/严格的层次模型.png" alt="严格的层次模型">
  <p align="center">
   <span>严格的层次模型</span>
  </p>
</p> 

- [x] **优点** ：
	> -  `易于控制` , 可信根CA主宰下级CA的运营权
	> -  `信任路径明确`

- [x] **缺点** ：
	> -  `风险集中` , 根CA的破坏将导致整个体系的破坏
	> - 认证关系要在CA建立时就要确立

##### 多CA层次模型中证书链示例

<p align="center">
  <img src="./img/多CA层次模型中证书链示例.png" alt="多CA层次模型中证书链示例">
  <p align="center">
   <span>示例</span>
  </p>
</p> 

#### 分布式信任结构模型

<p align="center">
  <img src="./img/分布式信任结构模型.png" alt="分布式信任结构模型">
  <p align="center">
   <span>分布式信任结构模型</span>
  </p>
</p> 

- [x] **优点** ：
	> - 网状信任模型把信任分散到两个或多个CA上， `健壮性 (robustness)好` 。
	> - CA间通过 `交叉认证` 在不同的CA之间建立信任。
	> - 用户只需要与给其颁发证书的CA建立信任关系，容易接入新的群体， `可扩展性(Scalability)好`

- [x] **缺点** ：
	> - 证书链不确定，可能会很长。
	> - 存在多个选择，也可能存在环路。

##### 证书链————交叉认证

<p align="center">
  <img src="./img/证书链————交叉认证.png" alt="证书链————交叉认证">
  <p align="center">
   <span>证书链————交叉认证</span>
  </p>
</p> 

> - 假设在短时间内已经验证了公钥和证书的绑定关系，也就是建立了信任关系，那么如果在下一次该域中又有需要验证的节点，则在缓存表中查找，如果在缓存表中有这个信任关系，那么就不用进行重复绑定了，在上述分布式的结构下也是如此。

#### 桥式结构

<p align="center">
  <img src="./img/桥式结构.png" alt="桥式结构">
  <p align="center">
   <span>桥式结构</span>
  </p>
</p> 

- [x] 采用桥型结构首先要建立一个 `桥CA(Bridge Certificate  Authority, BCA)`

- [x] 桥CA在不同的PKI体系之间起 `信任桥梁` 的作用，它不直接向用户签发证书，也不作为PKI体系中用户的一个信任锚点，只用来建立一个端到端的信任关系

#### 混合结构

<p align="center">
  <img src="./img/混合结构.png" alt="混合结构">
  <p align="center">
   <span>混合结构</span>
  </p>
</p> 

#### 分布式信任模型的特点

- [x] CA中心相对独立

- [x] 风险分散

- [x] 桥式CA的作用的只是认证范围的扩展或收缩，可以兼容已有CA中心

#### 美国金融领域联邦桥电子认证

<p align="center">
  <img src="./img/美国金融领域联邦桥电子认证.png" alt="美国金融领域联邦桥电子认证">
  <p align="center">
   <span>美国金融领域联邦桥电子认证</span>
  </p>
</p> 

#### 加拿大层次结构PKI体系

<p align="center">
  <img src="./img/加拿大层次结构PKI体系.png" alt="加拿大层次结构PKI体系">
  <p align="center">
   <span>加拿大层次结构PKI体系</span>
  </p>
</p> 

#### 国家PKI的具体发展思路

<p align="center">
  <img src="./img/国家PKI的具体发展思路.png" alt="国家PKI的具体发展思路">
  <p align="center">
   <span>国家PKI的具体发展思路</span>
  </p>
</p> 

##### 国家PKI组织结构

<p align="center">
  <img src="./img/国家PKI组织结构.png" alt="国家PKI组织结构">
  <p align="center">
   <span>国家PKI组织结构</span>
  </p>
</p> 

## 2.5 X.509标准

### PKI标准化

- [x] `X.509` ：是ISO和CCITT/ITU-T的X.500标准系列中的一部分，为了解决X.500目录中的身份鉴别和访问控制问题而设计的。同时本身也采用目录的形式进行管理和访问。在X.509中采用了大量的篇幅来定义证书和CRL的数据格式。

- [x] `PKIX工作组` ： IETF负责制定、标准化PKI及X.509研究的工作组。成立于1995年，旨在使得X.509标准中所做的证书和证书撤销列表工作适用于Internet中的需要。
	> - **证书和证书撤销列表、证书管理、操作、策略和认证管理陈述结构**

- [x] `LDAP(Lightweight Directory Access Protocol)` ：是轻量级目录访问协议，是X.500标准中的目录访问协议DAP的一个子集。还包含兼容性的内容。

- [x] `ANSI X9F` ：美国国家标准协会(ANSI)X9委员会(负责金融服务)开发的金融服务工业标准。

- [x] `ISO TC68` ：第8工作组，隶属于ISO中第68技术委员会下属的第2子委员会(记作ISO TC68/SC2/WG8，简称TC68)，从事公钥技术的标准化，主要服务于金融业。

- [x] `S/MIME` ：(Multipart Internet Mail Extensions)Email的加密规范增加了PKI概念，如证书格式、证书整理及证书撤消。

- [x] `SET` ：安全电子交易(the Secure Electronic Transaction),保证电子交易的安全性。

### PKI标准化主要内容

- [x] `基本安全算法` 各种公钥通信安全协议、对称DES算法、非对称RSA算法、散列函数及数字签名标准(DSS)等

- [x] `公钥基础设施` ASN.1规范、CA证书格式、Internet X.509 PKI标准、PKIX的主要内容、SET安全协议标准等

- [x] `E-mail安全` 安全电子邮件标准、加密报文语法、协议、报文规范、增强安全服务等。S/MIME、PEM、PGP等

- [x] `Web安全` S/HTTP协议及安全套接层协议SSL标准

### 中国PKI现状

- [ ] 中国的CA中心建设从1998年底开始。第一个电信行业CA————CTCA

- [ ] 2001年成立中国PKI论坛

- [ ] 三类CA中心
	> - `行业性CA中心` 中国金融认证中心(CFCA,http://www.cfca.com.cn/)
	> > - 金融：建行、招商、中行、工行、农行、交行
	> 
	> - `区域性CA中心` 
	> > - 北京、上海、广东、山东、湖北、安徽CA中心
	> > - 上海CA中心（ http://www.sheca.com/default.aspx)
	> > - 安徽CA中心（ http://www.aheca.cn/ ）
	> 
	> - `商业性CA中心` 企业创办的认证机构

- [ ] 截止2018年，上海CA累计发放数字证书1475万张，在用证书用户近500万。

- [ ] 截止2007年底，全国CA认证中心一共有140余家，其中具有信产部颁发的资质有24家， 2017年具有资质的企业达到43 家，一共颁发证书3.41 亿份

### 国内有关PKI法规方面的建设

- [ ] 02年，国务院信息办组织成立《国家PKI体系研究》，制定国家PKI总体框架，02年6月提交《国家PKI总体框架》

- [ ] 国内关于电子签名法的立法： 
	> - 2000年人大第一号提案
	> - 2002年信息产业部《电子签章法规》
	> - 2003年国务院法制办立法项目：名称《电子签名法》
	> - 2004年8月28日十届全国人大常委会第十一次会议表决通过电子签名法， 05年4月1日起施行。该法首次赋予电子签名与文本签名具有同等法律效力，并明确电子认证服务市场准入制度，保障电子交易安全。

- [ ] 09年2月4日，工业和信息化部第6次部务会议审议通过《电子认证服务管理办法》，作为第一号令进行颁发，自09年3月31日起施行。

- [ ] 16年11月，第十二届全国人民代表大会常务委员会第二十四次会议通过《中华人民共和国网络安全法》

- [ ] 18年，全国信息安全标准化技术委员会发布《电子认证2.0白皮书 》。

- [ ] 21年6月，第十三届全国人民代表大会常务委员会第二十九次会议通过《数据安全法》

- [ ] 21年8月20日，第十三届全国人民代表大会常务委员会第三十次会议通过《中华人民共和国个人信息保护法》

### 面临的问题

- [x] 仍然缺少相关法律的有效支持

- [x] 缺乏统一的行业技术标准

- [x] 与国外CA的交叉认证问题

- [x] 相关应用软件开发较少，已有开发应用还不够广泛

- [x] 实际使用过程中的可信度仍不完全被看好

### 解决措施

- [ ] 出台相关法规和统一技术标准

- [ ] 建立CA联盟，实现交叉认证

- [ ] 建设相应的应用系统，拓展市场

### X.509标准

- [x] ITU-T X.509 

- [x] 也是是信息技术-开放系统互连-目录-第8部分：鉴别框架(ISO/IEC 9594-8)

- [x] 目前使用最多的为V3版本，V4版本还在标准化当中，PKI是在X.509基础上发展起来的

- [x] 内容包括
	> - OSI参考模型安全体系结构定义-引用X.800的定义(安全假设)
	> - 目录模型定义-引用X.501对目录模型的定义(维护和管理)
	> - 公钥证书框架-对应认证
	> - 属性证书框架-对应访问控制中的权限管理
	> - CRL框架

> - 后三者也就是证书和CRL

- [x] 数字证书也叫电子证书，简称证书。数字证书、电子证书和证书都是X.509公钥证书的同义词，目前在用的要求符合 `ITU-T X.509 V3标准` 。

- [x] 版本更替
	> - X.509v1最早于1988年颁布
	> - X.509v2在1993年引入主体和签发者唯一标识符的概念
	> - X.509v3发布于1997年，支持扩展
	> - X.509v4&v5支持更多的扩展，并对CRL进行扩展，引入属性证书的概念，提出特权管理基础设施和授权模型。

> - `3A` 中有 `计费` ，而不是 `审计`

- [x] X.509标准的⽬的是什么？
	> - X.509：是ISO和CCITT/ITU-T的X.500标准系列中的⼀部分，为了解决X.500⽬录中的身份鉴别和访问控制问题⽽设计的。同时本身也采⽤⽬录的形式进⾏管理和访问。在X.509中采⽤了⼤量的篇幅来定义证书和CRL的数据格式。

### 证书的表示

- `CA《A》＝CA{V, SN, AI, CA, UCA, A, UA, Ap, TA，EXT}`
	> - `V` 证书版本号
	> - `SN` 证书 **序列号**
	> - `AI` 用于对证书进行签名的算法的 **标识符**
	> - `CA` CA名称
	> - `UCA` CA可选的唯一 **标识符**
	> - `A` 用户名称
	> - `UA` 用户A可选的唯一 **标识符**
	> - `Ap` 用户A的公钥
	> - `TA` 指出证书的有效期，包含两个日期，只有处于这两个日期之间才有效。
	> - `EXT` 扩展项 

#### 证书包含的内容

<p align="center">
  <img src="./img/证书包含的内容.png" alt="证书包含的内容">
  <p align="center">
   <span>证书包含的内容</span>
  </p>
</p> 

#### X.509证书格式

<p align="center">
  <img src="./img/X509证书格式.png" alt="X.509证书格式">
  <br>
  <br>
  <img src="./img/X509证书格式1.png" alt="X.509证书格式">
  <p align="center">
   <span>X.509证书格式</span>
  </p>
</p> 

### X.509v3证书中的扩展项

- [ ] 密钥扩展
	> - 主体公钥标识、密钥用途、私钥有效期

- [ ] 策略扩展
	> - CA承认的证书策略、策略映射

- [ ] 主体和签发者信息扩展
	> - 主体代用名、CA代用名、用户主体目录属性

- [ ] 认证路径扩展
	> - 基本约束、名称约束、策略约束

- [ ] CRL扩展
	> - CRL分布点地址

### 密钥管理问题和对对称密码的影响

- [x] 密钥管理是指在加密通信或加密数据存储中，有效地生成、分发、使用和存储密钥的过程。密钥管理是信息安全中的关键问题，因为密钥的泄露或不当使用可能导致数据泄露、信息被篡改、身份验证失败等安全问题。

- [x] 密钥管理对对称密码算法的影响尤为重要，因为对称密码算法使用相同的密钥来加密和解密数据。以下是密钥管理问题如何影响对称密码的一些方面：
	> - 生成强密钥：对称密码算法需要使用高强度的密钥才能提供足够的安全性。因此，密钥管理系统必须能够生成足够强度的密钥，以防止被暴力破解或推导出明文。
	> - 安全地分发密钥：对称密码算法要求通信双方共享相同的密钥。在实际应用中，安全地将密钥分发给通信方是至关重要的。传统上，这通常通过安全信道或密钥交换协议来实现。
	> - 保护密钥的存储和传输：密钥在存储和传输过程中容易受到攻击。密钥管理系统必须能够保护密钥免受未经授权的访问或篡改。这可能涉及使用加密算法对密钥进行加密、访问控制和密钥审计等措施。
	> - 密钥更新和轮换：密钥可能会因为泄露或失效而需要更新或轮换。密钥管理系统必须能够有效地管理密钥的生命周期，包括定期更新或轮换密钥，以确保系统的安全性。
	> - 密钥丢失和备份：密钥丢失可能会导致数据无法解密或访问。因此，密钥管理系统需要提供密钥备份和恢复机制，以防止密钥丢失或损坏。

## 2.6 认证机构CA系统

### 认证机构CA

- [x] PKI核心实体是 `认证机构CA` ，为各个实体颁发电子证书，对实体身份信息和相应公钥数据进行 `数字签名` ，用以 `绑定该实体的公钥和身份` ，以证明各实体在网上身份的真实性；并负责在交易中检验和管理证书。同时也是 `CRL的签发者` 。

### CA系统功能

- [ ] 处理证书申请，在线申请和离线申请

- [ ] 证书审批( `可以由RA来承担` )

- [ ] 证书颁发，在线发放和离线发放

- [ ] 证书撤消
	> - 密钥泄露、从属关系变更、终止使用、CA本身原因

- [ ] 证书更新，人工方式和自动方式

- [ ] 证书撤销列表(CRL)管理

- [ ] 证书的归档

- [ ] CA自身的维护管理

- [ ] CA自身密钥管理

### OpenCA介绍

- [x] 开源项目，旨在构建一个功能强大的、健壮的CA 系统

- [x] 环境：Linux，Perl，OpenSSL，Apache Web Server，MySQL，OpenSSL 

<p align="center">
  <img src="./img/OpenCA介绍.png" alt="OpenCA介绍">
  <p align="center">
   <span>OpenCA</span>
  </p>
</p> 

### 其他开源方案

- [x] EJBCA CE
	> - https://www.ejbca.org/

- [x] Dogtag Certificate System
	> - https://www.dogtagpki.org

- [x] OpenXPKI
	> - https://www.openxpki.org/

- [x] Step-ca
	> - https://smallstep.com/docs/step-ca/

# 第三章：IPSec:AH和ESP 

## 3.1 IPSec协议的引入

### IP Security Protocols

- [x] `IPSec(IP Security)` 是Internet的网络层安全协议, 于1995年8月发布IPSec1.0, 1998年11月发布了IPSec2.0, 同时支持IPv4和IPv6, 它规定了：
	> - IPSec的整体结构(RFC4301, 2401)
	> - IPSec协议AH和ESP(认证与加密)(RFC4302, 4303, 4305, 2401-2406)
	> - 密钥管理协议IKE(RFC4304，4306，2412)

### IPSec RFCs

<p align="center">
  <img src="./img/IPSec RFCs.png" alt="IPSec RFCs">
  <p align="center">
   <span>IPSec RFCs</span>
  </p>
</p> 

### 为什么需要IPSec？

- [x] 传统计算机网络没有考虑安全需求，安全性能差，存在众多安全隐患。
	> - 如伪造、篡改、重放、窃听

- [x] 可以在网络层建立 `端到端` 保护的 `安全隧道(Secure Tunnel)` ，可以对上层应用，或者对用户透明
	> - 保护IP数据包的保密性(via，分组的对称加密)
	> - 验证IP包的来源以及是否完好无损(via，HMAC)
	> - 防止IP数据包被重放(via，随机数、时间戳)

- [x] 安全保护的可能范围
	> - `点到点(链路)` ：由于IP分组头要用来寻路，在路由器上需要相应的安全操作(如认证或加解密)
	> - `端到端` ：只需要在收发两端进行安全操作

### Security Protocol Layers

<p align="center">
  <img src="./img/Security Protocol Layers.png" alt="Security Protocol Layers">
  <p align="center">
   <span>Security Protocol Layers</span>
  </p>
</p> 

## 3.2 IPv4和IPv6协议

<p align="center">
  <img src="./img/Security Protocol Layers.png" alt="Security Protocol Layers">
  <p align="center">
   <span>Security Protocol Layers</span>
  </p>
</p> 

### IPv4协议—Internet的网络层协议

- [x] IPv4协议—Internet的网络层协议

<p align="center">
  <img src="./img/IPv4协议—Internet的网络层协议.png" alt="IPv4协议—Internet的网络层协议">
  <p align="center">
   <span>IPv4协议—Internet的网络层协议</span>
  </p>
</p> 

### IPv6协议的引入

<p align="center">
  <img src="./img/IPv6协议的引入.png" alt="IPv6协议的引入">
  <p align="center">
   <span>IPv6协议的引入</span>
  </p>
</p> 

#### IPv6协议

<p align="center">
  <img src="./img/IPv6协议.png" alt="IPv6协议">
	<br>
	<br>
	<img src="./img/IPv6协议1.png" alt="IPv6协议">
  <p align="center">
   <span>IPv6协议</span>
  </p>
</p> 

#### IPv6扩展头标顺序

<p align="center">
  <img src="./img/IPv6扩展头标顺序.png" alt="IPv6扩展头标顺序">
  <p align="center">
   <span>IPv6扩展头标顺序</span>
  </p>
</p> 

#### Data in TCP/IP

<p align="center">
  <img src="./img/Data in TCPIP.png" alt="Data in TCP/IP">
  <p align="center">
   <span>Data in TCP/IP</span>
  </p>
</p> 

#### Data in TCP/IPSec/IP

<p align="center">
  <img src="./img/Data in TCPIPSecIP1.png" alt="Data in TCP/IPSec/IP">
	<br>
	<br>
	<img src="./img/Data in TCPIPSecIP2.png" alt="Data in TCP/IPSec/IP">
  <p align="center">
   <span>Data in TCP/IPSec/IP</span>
  </p>
</p> 

## 3.3 IPSec中的安全组合（SA）
## 3.4 认证头标AH
## 3.5 封装安全载荷头标ESP
## 3.6 IPSec的传输模式与隧道模式
## 3.7 IPSec与NAT
## 3.8 IPSec隧道模式的应用-VPN
## 3.9 IPSec的实现

# 第四章：IPSec-IKE   
# 第五章：SSL/TLS协议  
# 第六章：防火墙与NAT
# 第七章：虚拟专用网VPN   
# 第八章：应用层安全协议  
# 第九章：无线局域网安全  
