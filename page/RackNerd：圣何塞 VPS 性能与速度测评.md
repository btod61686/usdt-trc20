# RackNerd：圣何塞 VPS 性能与速度测评

近期，RackNerd推出了限时春节促销活动，我也顺手入手了一台位于圣何塞的VPS，专供测试使用。这篇文章将详细测评这款圣何塞 VPS的性能和速度，希望可以提供参考。顺便提一句，RackNerd促销活动确实值得关注，以下是相关信息：

👉 [【建议收藏】2025年Racknerd最新优惠套餐整理汇总 - 每日更新可用活动优惠](https://bit.ly/Rack_Nerd)

---

## 1. 服务器配置概览

测试服务器位于美国西海岸圣何塞，接入 1Gbps 带宽，基于 KVM 虚拟化架构，存储是纯 SSD RAID10，提供稳定高性能。以下是具体的硬件配置：

- **套餐**：1.5 GB SSD KVM VPS Special
- **处理器**：1x vCPU Core（Intel Xeon E5-2680 v2 @ 2.80GHz）
- **硬盘空间**：20 GB纯SSD RAID-10存储
- **内存**：1.5 GB
- **带宽**：3000GB/月，优质带宽
- **公网端口**：1Gbps
- **IPv4地址**：1个独立地址
- **可选机房**：圣何塞、纽约、亚特兰大、阿姆斯特丹

价格方面，年度套餐仅需 $13.99，非常具有竞争力。

---

## 2. 系统规格与测试详情

### 系统信息

服务器运行环境如下：

plaintext
CPU Model             : Intel(R) Xeon(R) CPU E5-2680 v2 @ 2.80GHz
CPU Cores             : 1
CPU Frequency         : 2799.998 MHz
CPU Cache             : 16384 KB
Total Disk            : 19.0 GB (1.7 GB Used)
Total Mem             : 1494 MB (140 MB Used)
Total Swap            : 1535 MB (0 MB Used)
System uptime         : 1 days, 3 hour 46 min
Load average          : 0.00, 0.01, 0.05
OS                    : CentOS 7.9.2009
Arch                  : x86_64 (64 Bit)
Kernel                : 3.10.0-1160.15.2.el7.x86_64
TCP CC                : cubic
Virtualization        : KVM
Location              : San Jose / US


---

### 磁盘性能测试

圣何塞机房的磁盘速度较为优异，以下是测试数据：

plaintext
I/O Speed(1st run)    : 809 MB/s
I/O Speed(2nd run)    : 945 MB/s
I/O Speed(3rd run)    : 744 MB/s
Average I/O speed     : 832.7 MB/s


支持 AES-NI 和 VM-x/AMD-V 的硬件加速特性，性能表现良好。

---

## 3. 网络测速与路由分析

### Speed测速

不同网络环境下测速结果如下：
- **电信**：表现稳定，速度中规中矩。
- **移动**：测试数据表明移动线路表现最佳。
- **联通**：与电信相当。

此外，iperf3 测试显示服务器在欧洲地区的网络速度表现同样优异，非常适合外部连接的使用场景。

---

### 路由跟踪

路由测试显示不同线路的优缺点：
- **电信线路**：去程和回程均为直连圣何塞，延迟较低。
- **移动线路**：回程通过日本 NTT，中途到香港后才转入国内网络。
- **联通线路**：回程通过圣何塞 NTT 机房，直接连入国内联通线路，整体路由较为简单。

以下是部分 traceroute 数据结果：

plaintext
Traceroute to China, Beijing CM (TCP Mode, Max 30 Hop)
============================================================
traceroute to 211.136.25.153 (211.136.25.153), 30 hops max, 60 byte packets
 1  75.127.0.25  1.41 ms  AS36352  United States California San Jose colocrossing.com
 ...
13  *
14  *
15  *
16  *
17  221.176.27.253  190.14 ms  AS9808  China Beijing ChinaMobile
...


从结果可以看出，该 VPS的线路适合移动用户，电信和联通用户体验较为相似。

---

## 4. 性能跑分和其他测试

### Unixbench跑分

在 Unixbench 跑分测试中，CPU性能表现结果为 734 分。如果切换到 AMD 和更新架构的 CPU，跑分可能会更高。

### 超内存测试

内存性能表现如下：在超负荷测试中，内存稳定分配到 2790MB 时进程被 killed，性能令人满意。

plaintext
2630MB allocated
2640MB allocated
...
2790MB allocated
Killed


---

## 5. 总结

通过这次测试，圣何塞机房的性能和网络表现令人满意。线路对移动用户较为友好，电信和联通均表现平稳。年度费用仅为 $13.99，性价比在同类产品中优胜。如果能抓住促销活动，价格还能进一步降低，非常适合预算有限却需要性能可靠的用户选择！

👉 [【建议收藏】2025年Racknerd最新优惠套餐整理汇总 - 每日更新可用活动优惠](https://bit.ly/Rack_Nerd)