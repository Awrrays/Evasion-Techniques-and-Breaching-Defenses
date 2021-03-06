# Evasion-Techniques-and-Breaching-Defenses
Evasion Techniques and Breaching Defenses大纲

- [规避技术和突破防御](#---------)
  * [2 - 操作系统与编程理论](#2------------)
    + [2.1 编程理论](#21-----)
      - [2.1.1 编程语言级别](#211-------)
      - [2.1.2 编程概念](#212-----)
    + [2.2 Windows 概念](#22-windows---)
      - [2.2.1 Windows 上的 Windows](#221-windows----windows)
      - [2.2.2 Win32 API](#222-win32-api)
      - [2.2.3 Windows 注册表](#223-windows----)
    + [2.3 总结](#23---)
  * [3 - 使用 Office 执行客户端代码](#3------office--------)
    + [3.1 你愿意做我的滴管吗](#31----------)
      - [3.1.1 分阶段与非分阶段有效载荷](#311-------------)
      - [3.1.2 构建我们的 Dropper](#312-------dropper)
      - [3.1.3 HTML走私](#313-html--)
    + [3.2 Microsoft Office 钓鱼](#32-microsoft-office---)
      - [3.2.1 安装微软Office](#321-----office)
      - [3.2.2 VBA 简介](#322-vba---)
      - [3.2.3 让PowerShell帮助我们](#323--powershell----)
    + [3.3 保持形象](#33-----)
      - [3.3.1 网络钓鱼 PreTexting](#331------pretexting)
      - [3.3.2 旧的 Switcheroo](#332----switcheroo)
    + [3.4 在字内存中执行Shellcode](#34--------shellcode)
      - [3.4.1 从 VBA 调用 Win32 API](#341---vba----win32-api)
      - [3.4.2 VBA Shellcode Runner](#342-vba-shellcode-runner)
    + [3.5 PowerShell Shellcode Runner](#35-powershell-shellcode-runner)
      - [3.5.1 从 PowerShell 调用 Win32 API](#351---powershell----win32-api)
      - [3.5.2 将 Shellcode Runner 移植到 PowerShell](#352---shellcode-runner-----powershell)
    + [3.6 将 PowerShell 保存在内存中](#36---powershell-------)
      - [3.6.1 添加类型编译](#361-------)
      - [3.6.2 利用 UnsafeNativeMethods](#362----unsafenativemethods)
      - [3.6.3 委托类型反射](#363-------)
      - [3.6.4 PowerShell 中的反射 Shellcode Runner](#364-powershell------shellcode-runner)
    + [3.7 与代理交谈](#37------)
      - [3.7.1 PowerShell 代理感知通信](#371-powershell-------)
      - [3.7.2 摆弄用户代理](#372-------)
      - [3.7.3 给我一个系统代理](#373---------)
    + [3.8 总结](#38---)
  * [4 - 使用 Windows 脚本宿主执行客户端代码](#4------windows------------)
    + [4.1 在 Jscript 中创建一个基本的 Dropper](#41---jscript----------dropper)
      - [4.1.1 在 Windows 上执行 Jscript](#411---windows-----jscript)
      - [4.1.2 Jscript Meterpreter Dropper](#412-jscript-meterpreter-dropper)
    + [4.2 Jscript 和 C#](#42-jscript---c-)
      - [4.2.1 Visual Studio 简介](#421-visual-studio---)
      - [4.2.2 DotNetToJ 脚本](#422-dotnettoj---)
      - [4.2.3 来自 C# 的 Win32 API 调用](#423----c----win32-api---)
      - [4.2.4 C#中的Shellcode Runner](#424-c---shellcode-runner)
      - [4.2.5 Jscript Shellcode Runner](#425-jscript-shellcode-runner)
      - [4.2.6 神枪手](#426----)
    + [4.3 重新审视内存中的 PowerShell](#43----------powershell)
      - [4.3.1 反射负载](#431-----)
    + [4.4 总结](#44---)
  * [5 - 进程注入和迁移](#5----------)
    + [5.1 为我们的 Shellcode 找到一个家](#51------shellcode------)
      - [5.1.1 过程注入和迁移理论](#511----------)
      - [5.1.2 C#中的进程注入](#512-c-------)
    + [5.2 DLL 注入](#52-dll---)
      - [5.2.1 DLL 注入理论](#521-dll-----)
      - [5.2.2 C# DLL 注入](#522-c--dll---)
    + [5.3 反射 DLL 注入](#53----dll---)
      - [5.3.1 反射DLL注入理论](#531---dll----)
      - [5.3.2 PowerShell 中的反射 DLL 注入](#532-powershell------dll---)
    + [5.4 工艺镂空](#54-----)
      - [5.4.1 过程空心理论](#541-------)
      - [5.4.2 C#中的进程挖空](#542-c-------)
    + [5.5 总结](#55---)
  * [6 - 防病毒规避简介](#6----------)
    + [6.1 杀毒软件概述](#61-------)
    + [6.2 模拟目标环境](#62-------)
    + [6.3 在文件中定位签名](#63---------)
    + [6.4 使用 Metasploit 绕过杀毒软件](#64----metasploit-------)
      - [6.4.1 Metasploit 编码器](#641-metasploit----)
      - [6.4.2 Metasploit 加密器](#642-metasploit----)
    + [6.5 用 C# 绕过杀毒软件](#65---c--------)
      - [6.5.1 C# Shellcode Runner vs Antivirus](#651-c--shellcode-runner-vs-antivirus)
      - [6.5.2 加密 C# Shellcode Runner](#652----c--shellcode-runner)
    + [6.6 摆弄我们的行为](#66--------)
      - [6.6.1 简单睡眠定时器](#661--------)
      - [6.6.2 非模拟 API](#662-----api)
    + [6.7 Office 请绕过杀毒软件](#67-office--------)
      - [6.7.1 在 VBA 中绕过杀毒软件](#671---vba--------)
      - [6.7.2 踩在 Microsoft Word 上](#672----microsoft-word--)
    + [6.8 在 VBA 中隐藏 PowerShell](#68---vba-----powershell)
      - [6.8.1 PowerShell Shellcode Runner的检测](#681-powershell-shellcode-runner---)
      - [6.8.2 使用 WMI 解链](#682----wmi---)
      - [6.8.3 混淆 VBA](#683----vba)
    + [6.9 总结](#69---)
  * [7 - 高级防病毒规避](#7----------)
    + [7.1 英特尔架构和 Windows 10](#71--------windows-10)
      - [7.1.1 WinDbg 介绍](#711-windbg---)
    + [7.2 反恶意软件扫描界面](#72----------)
      - [7.2.1 了解 AMSI](#721----amsi)
      - [7.2.2 与 Frida 挂钩](#722---frida---)
    + [7.3 在 PowerShell 中使用反射绕过 AMSI](#73---powershell---------amsi)
      - [7.3.1 什么语境妈妈？](#731--------)
      - [7.3.2 攻击初始化](#732------)
    + [7.4 在 PowerShell 中破坏 AMSI](#74---powershell-----amsi)
      - [7.4.1 理解装配流程](#741-------)
      - [7.4.2 内部补丁](#742-----)
    + [7.5 UAC 绕过 vs Microsoft Defender](#75-uac----vs-microsoft-defender)
      - [7.5.1 FodHelper UAC 绕过](#751-fodhelper-uac---)
      - [7.5.2 改进 Fodhelper](#752----fodhelper)
    + [7.6 在 JScript 中绕过 AMSI](#76---jscript-----amsi)
      - [7.6.1 检测 AMSI API 流](#761----amsi-api--)
      - [7.6.2 那是您的注册表项吗？](#762-----------)
      - [7.6.3 我是我自己的可执行文件](#763------------)
    + [7.7 总结](#77---)
  * [8 - 应用白名单](#8--------)
    + [8.1 应用白名单理论与设置](#81-----------)
      - [8.1.1 应用白名单理论](#811--------)
      - [8.1.2 AppLocker 设置和规则](#812-applocker------)
    + [8.2 基本绕过](#82-----)
      - [8.2.1 可信文件夹](#821------)
      - [8.2.2 绕过 DLL](#822----dll)
      - [8.2.3 备用数据流](#823------)
      - [8.2.4 第三方执行](#824------)
    + [8.3 使用 PowerShell 绕过 AppLocker](#83----powershell----applocker)
      - [8.3.1 PowerShell 约束语言模式](#831-powershell-------)
      - [8.3.2 自定义运行空间](#832--------)
      - [8.3.3 PowerShell CLM 绕过](#833-powershell-clm---)
      - [8.3.4 反射注入返回](#834-------)
    + [8.4 用 C# 绕过 AppLocker](#84---c-----applocker)
      - [8.4.1 定位目标](#841-----)
      - [8.4.2 负载逆向工程](#842-------)
      - [8.4.3 给我代码执行](#843-------)
      - [8.4.4 调用目标第 1 部分](#844-------1---)
      - [8.4.5 调用目标第 2 部分](#845-------2---)
    + [8.5 用 JScript 绕过 AppLocker](#85---jscript----applocker)
      - [8.5.1 JScript 和 MSHTA](#851-jscript---mshta)
      - [8.5.2 XSL 转换](#852-xsl---)
    + [8.6 总结](#86---)
  * [9 - 绕过网络过滤器](#9----------)
    + [9.1 DNS 过滤器](#91-dns----)
      - [9.1.2 处理 DNS 过滤器](#912----dns----)
    + [9.2 网络代理](#92-----)
      - [9.2.1 绕过网络代理](#921-------)
    + [9.3 IDS 和 IPS 传感器](#93-ids---ips----)
      - [9.3.1 案例研究：使用自定义证书绕过诺顿 HIPS](#931------------------hips)
    + [9.4 全包捕获设备](#94-------)
    + [9.5 HTTPS 检查](#95-https---)
    + [9.6 域前置](#96----)
      - [9.6.1 使用 Azure CDN 进行域前置](#961----azure-cdn------)
      - [9.6.2 实验室中的域前置](#962---------)
    + [9.7 DNS 隧道](#97-dns---)
      - [9.7.1 DNS 隧道如何工作](#971-dns-------)
      - [9.7.2 使用 dnscat2 的 DNS 隧道](#972----dnscat2---dns---)
    + [9.8 总结](#98---)
  * [10 - Linux 后漏洞利用](#10---linux------)
    + [10.1 用户配置文件](#101-------)
      - [10.1.1 VIM 配置简单后门](#1011-vim-------)
      - [10.1.2 VIM 配置简单的键盘记录器](#1012-vim-----------)
    + [10.2 绕过AV](#102---av)
      - [10.2.1 卡巴斯基端点安全](#1021---------)
      - [10.2.2 Antiscan.me](#1022-antiscanme)
    + [10.3 共享库](#103----)
      - [10.3.1 共享库如何在 Linux 上工作](#1031--------linux----)
      - [10.3.2 通过 LD_LIBRARY_PATH 劫持共享库](#1032----ld-library-path------)
      - [10.3.3 通过 LD_PRELOAD 进行利用](#1033----ld-preload-----)
    + [10.4 总结](#104---)
  * [11 - 自助服务亭突围](#11----------)
    + [11.1 信息亭枚举](#111------)
      - [11.1.1 Kiosk 浏览器枚举](#1111-kiosk------)
    + [11.2 命令执行](#112-----)
      - [11.2.1 探索文件系统](#1121-------)
      - [11.2.2 利用 Firefox 配置文件](#1122----firefox-----)
      - [11.2.3 枚举系统信息](#1123-------)
      - [11.2.4 划伤表面](#1124-----)
    + [11.3 后期开发](#113-----)
      - [11.3.1 模拟交互式外壳](#1131--------)
    + [11.4 权限提升](#114-----)
      - [11.4.1 跳出框框思考](#1141-------)
      - [11.4.2 时刻顶部的根壳](#1142--------)
      - [11.4.3 获取root终端访问权限](#1143---root------)
    + [11.5 Windows Kiosk 突围技术](#115-windows-kiosk-----)
    + [11.6 总结](#116---)
  * [12 - Windows 凭据](#12---windows---)
    + [12.1 本地 Windows 凭据](#121----windows---)
      - [12.1.1 SAM 数据库](#1211-sam----)
      - [12.1.2 加固本地管理员账户](#1212----------)
    + [12.2 访问令牌](#122-----)
      - [12.2.1 访问令牌理论](#1221-------)
      - [12.2.2 模拟提升](#1222-----)
      - [12.2.3 隐身乐趣](#1223-----)
    + [12.3 Kerberos 和域凭据](#123-kerberos-----)
      - [12.3.1 Kerberos 认证](#1231-kerberos---)
      - [12.3.2 模仿](#1232---)
    + [12.4 离线处理凭证](#124-------)
      - [12.4.1 内存转储](#1241-----)
      - [12.4.2 MiniDumpWriteDump](#1242-minidumpwritedump)
    + [12.5 总结](#125---)
  * [13 - Windows横向移动](#13---windows----)
    + [13.1 远程桌面协议](#131-------)
      - [13.1.1 RDP 横向运动](#1311-rdp-----)
      - [13.1.2 使用 Metasploit 进行反向 RDP 代理](#1312----metasploit------rdp---)
      - [13.1.3 使用 Chisel 进行反向 RDP 代理](#1313----chisel------rdp---)
      - [13.1.4 RDP 作为控制台](#1314-rdp------)
      - [13.1.5 从 RDP 窃取明文凭据](#1315---rdp-------)
    + [13.2 无文件横向移动](#132--------)
      - [13.2.1 认证与执行理论](#1321--------)
      - [13.2.2 在 C# 中实现无文件横向移动](#1322---c------------)
    + [13.3 总结](#133---)
  * [14 - Linux横向运动](#14---linux----)
    + [14.1 SSH 横向移动](#141-ssh-----)
      - [14.1.1 SSH 密钥](#1411-ssh---)
      - [14.1.2 SSH 持久化](#1412-ssh----)
      - [14.1.3 ControlMaster SSH 劫持](#1413-controlmaster-ssh---)
      - [14.1.4 使用 SSH-Agent 和 SSH Agent Forwarding 进行 SSH 劫持](#1414----ssh-agent---ssh-agent-forwarding----ssh---)
    + [14.2 开发运营](#142-----)
      - [14.2.1 Ansible 简介](#1421-ansible---)
      - [14.2.2 枚举 Ansible](#1422----ansible)
      - [14.2.3 临时命令](#1423-----)
      - [14.2.4 Ansible 剧本](#1424-ansible---)
      - [14.2.5 利用剧本获取 Ansible 凭证](#1425--------ansible---)
      - [14.2.6 Ansible Playbook 的弱权限](#1426-ansible-playbook-----)
      - [14.2.7 通过 Ansible 模块泄露敏感数据](#1427----ansible---------)
      - [14.2.8 Artifactory 介绍](#1428-artifactory---)
      - [14.2.9 人工枚举](#1429-----)
      - [14.2.10 破坏 Artifactory 备份](#14210----artifactory---)
      - [14.2.11 破坏 Artifactory 的数据库](#14211----artifactory-----)
      - [14.2.12 添加辅助 Artifactory 管理员帐户](#14212------artifactory------)
    + [14.3 Linux 上的 Kerberos](#143-linux----kerberos)
      - [14.3.1 Linux 上的 Kerberos 概述](#1431-linux----kerberos---)
      - [14.3.2 窃取 Keytab 文件](#1432----keytab---)
      - [14.3.3 使用凭证缓存文件进行攻击](#1433-------------)
      - [14.3.4 使用带有 Impacket 的 Kerberos](#1434------impacket---kerberos)
    + [14.4 总结](#144---)
  * [15 - Microsoft SQL 攻击](#15---microsoft-sql---)
    + [15.1 Active Directory 中的 MS SQL](#151-active-directory----ms-sql)
      - [15.1.1 MS SQL 枚举](#1511-ms-sql---)
      - [15.1.2 MS SQL 认证](#1512-ms-sql---)
      - [15.1.3 UNC 路径注入](#1513-unc-----)
      - [15.1.4 中继我的哈希](#1514-------)
    + [15.2 MS SQL 升级](#152-ms-sql---)
      - [15.2.1 权限提升](#1521-----)
      - [15.2.2 获取代码执行](#1522-------)
      - [15.2.3 自定义组件](#1523------)
    + [15.3 链接的 SQL Server](#153-----sql-server)
      - [15.3.1 跟随链接](#1531-----)
      - [15.3.2 回家给我](#1532-----)
    + [15.4 总结](#154---)
  * [16 - 活动目录利用](#16---------)
    + [16.1 AD 对象安全权限](#161-ad-------)
      - [16.1.1 对象权限理论](#1611-------)
      - [16.1.2 滥用 GenericAll](#1612----genericall)
      - [16.1.3 滥用 WriteDACL](#1613----writedacl)
    + [16.2 Kerberos 委托](#162-kerberos---)
      - [16.2.1 无约束委派](#1621------)
      - [16.2.2 我是域控制器](#1622-------)
      - [16.2.3 约束委托](#1623-----)
      - [16.2.4 基于资源的约束委托](#1624----------)
    + [16.3 Active Directory 森林理论](#163-active-directory-----)
      - [16.3.1 森林中的 Active Directory 信任](#1631------active-directory---)
      - [16.3.2 森林中的枚举](#1632-------)
    + [16.4 烧毁森林](#164-----)
      - [16.4.1 拥有具有额外 SID 的林](#1641--------sid---)
      - [16.4.2 拥有打印机林](#1642-------)
    + [16.5 超越森林](#165-----)
      - [16.5.1 林之间的 Active Directory 信任](#1651------active-directory---)
      - [16.5.2 超越森林的枚举](#1652--------)
    + [16.6 破坏额外的森林](#166--------)
      - [16.6.1 给我看看你的额外 SID](#1661----------sid)
      - [16.6.2 林中链接的 SQL Server](#1662-------sql-server)
    + [16.7 总结](#167---)
  * [17 - 组合碎片](#17-------)
    + [17.1 枚举和外壳](#171------)
      - [17.1.1 初始枚举](#1711-----)
      - [17.1.2 获得初步立足点](#1712--------)
      - [17.1.3 开发后枚举](#1713------)
    + [17.2 攻击委托](#172-----)
      - [17.2.1 web01 权限提升](#1721-web01-----)
      - [17.2.2 获取哈希](#1722-----)
      - [17.2.3 委托我的票](#1723------)
    + [17.3 拥有域](#173----)
      - [17.3.1 横向运动](#1731-----)
      - [17.3.2 成为域管理员](#1732-------)
    + [17.4 总结](#174---)
