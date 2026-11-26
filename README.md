# 洛杉矶VPS选购指南：SixtyNet 全套餐多少钱？住宅 IP 能不能建站？AS9929 大带宽又适合谁？（附年付价格换算与端口限制）

SixtyNet 洛杉矶目前最便宜的一档是 LAX-STARTER，**$200/年**，2 核 2G、40G NVMe、5TB 月流量、2Gbps 端口，折合每月约 $16.7。这个价在洛杉矶不算低，同样 2 核 2G，年付二三十美元的国际线路机器也有人卖。差价主要花在两个地方：一是 2Gbps 起步的端口和 DDoS 防护，二是 SixtyNet 另一条别的商家做得不多的产品线，带住宅 IP 的 Residential 系列。

下面把官网在售的 12 个套餐全部摊开，再讲清三件容易买错的事：住宅 IP 那几档为什么封了 80 和 443、标了 AS9929 的档位贵在哪、年付价换算成月均之后它和洛杉矶其他家差多少。

## 选购速览

> 建站、跑 API、做流量中转，不需要住宅 IP：**LAX-STARTER，$200/年**（2 核 2G/40G/5TB/2Gbps），配置和价格最平衡的一档。
>
> 要住宅 IP 做流媒体解锁、账号环境、广告投放：**Residential-STARTER，$260/年**。下单前先确认业务不需要 80 和 443 端口。
>
> 既要住宅 IP、又要页面明确写了联通 AS9929 优化：**IRVINE-PRO-STARTER，$350/年**，这一档退款只退到网站余额。
>
> 要做 BGP 广播、按 95th 计费的大带宽：China Unicom-Premium，$2,500/年。

👉 [查看 SixtyNet 洛杉矶全部套餐的年付价格](https://sixtynet.net/aff.php?aff=39)

## SixtyNet 洛杉矶在售套餐：12 档配置与年付价格

官网 VPS Hosting 页面标的都是年繳价（Annually），没有月付标价。下表价格一栏是折后年价，括号里是页面同时显示的原价。

| 套餐 | CPU、内存 | 存储 | 流量、端口 | 年繳价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| LAX-STARTER | 2 核 / 2G | 40G NVMe | 5TB / 2Gbps | $200（原 $240） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 核 / 4G | 80G NVMe | 10TB / 4Gbps | $400（原 $480） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 核 / 8G | 160G NVMe | 20TB / 10Gbps | $800（原 $960） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 核 / 16G | 320G NVMe | 40TB / 10Gbps | $1,600（原 $1,920） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-500G | 4 核 / 4G | 300G + 200G RAID10 | 10TB / 10Gbps | $400（原 $480） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| Residential-STARTER | 2 核 / 2G | 40G NVMe | 5TB / 2Gbps | $260（原 $300） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| Residential-MICRO | 4 核 / 4G | 80G NVMe | 10TB / 4Gbps | $460（原 $540） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| Residential-MEDIUM | 8 核 / 8G | 160G NVMe | 20TB / 10Gbps | $860（原 $1,020） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| Residential-LARGE | 16 核 / 16G | 320G NVMe | 40TB / 10Gbps | $1,660（原 $1,980） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| IRVINE-PRO-STARTER | 2 核 / 2G | 40G NVMe | 5TB / 2Gbps | $350（原 $420） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| IRVINE-PRO-MICRO | 4 核 / 4G | 80G NVMe | 10TB / 4Gbps | $550（原 $660） | [ 查看](https://sixtynet.net/aff.php?aff=39) |
| China Unicom-Premium | 页面未标 | 页面未标 | 100M 基础带宽，3 倍突发 | $2,500（原 $3,000） | [ 查看](https://sixtynet.net/aff.php?aff=39) |

有两点表格里放不下：

- 除 China Unicom-Premium 外，所有套餐都标了 12500 或 25000 IOPS 的 NVMe，端口从 2Gbps 到 10Gbps 分档，配置表和价格档位基本是一一对应的。
- 官网还有一个 8 核 8G、700G + 300G RAID10、15TB 流量的存储档，页面上只列了配置，没标价格，要买得单独问。

同一价位下，各系列拉开差距的地方在 IP 属性和端口策略，CPU 和内存反而接近。

| 系列 | IP 属性 | 中国方向线路 | 端口与访问限制 |
| --- | --- | --- | --- |
| LAX | 普通机房 IP | 页面未标优化 | 全端口可用，带 DDoS 防护 |
| LAX-Storage | 普通机房 IP | 页面未标优化 | 全端口可用，RAID10 大容量 |
| Residential | 住宅 IP | 页面未标优化 | 不开放 80、443 |
| IRVINE-PRO | 住宅 IP | AS9929 | 不开放 80、443，拒绝所有外部探测与扫描，退款只退余额 |
| China Unicom-Premium | 页面未标 | AS9929 | 100M 基础带宽，3 倍突发，95th 计费，免费 BGP session |

China Unicom-Premium 的产品页还提到季付和年付都有折扣，想先小规模试这条线，可以问一下季付的报价。

## 线路怎么选：AS9929、CN2 和三网直连差在哪

洛杉矶机房对国内用户的价值，在于它是跨太平洋光缆在美国本土的主要落点，回国路由的可选余量大。真正决定体验和价格的是走哪条线，业内大致分三档：

- **CN2 GIA**：电信精品网，延迟低、晚高峰丢包少，带宽给得小、价格高，联通和移动用户受益有限。
- **联通 AS9929**：联通精品网，回程质量好，价格介于 CN2 GIA 和普通 BGP 之间，预算有限又想要稳定回国的常见折中。
- **三网直连 BGP**：电信 163 + 联通 4837 + 移动 CMI，三家各走各的骨干，不偏科，价格最亲民。

SixtyNet 页面上明确写 AS9929 的只有两个系列：IRVINE-PRO 和 China Unicom-Premium。LAX 和 Residential 系列没有标中国优化线路。近期一份第三方测评测的是 Cox 住宅 IP 那批机器，给出的路由是电信去程走 CN2 直连洛杉矶、联通去程直连后接 GTT、移动去程直连；回程电信和移动走 CN2，联通走 AS10099 + AS9929。同一份测评提到官方屏蔽了 PING 和 80/443 端口。

这些是测评当时的实测结果，不是官网承诺。同一系列换批次，上游运营商可能从 Cox 换成 AT&T 或其他，路由跟着变，页面上的线路标注和到手机器的实际路由要分开看。想确认当前批次，下单前找客服要测试 IP 最直接。

## 住宅 IP 值不值这个价？先看 80 和 443 端口

住宅 IP 卖的是“看起来像普通家庭宽带”。流媒体平台、电商账号、支付风控、广告投放后台判断的多是 IP 的 ISP 属性，机房 IP 段早被标成数据中心，住宅 IP 段则显示成 AT&T、Cox 这类运营商。第三方测评对 SixtyNet 住宅 IP 的判断是原生美国 IP、双 ISP 住宅属性、流媒体解锁较好。

代价写在产品页上：**住宅 IP 产品不开放 80 和 443 端口**，理由是 IP 风控。这两个端口一封，实际影响是：

- 不能直接跑 HTTP/HTTPS 网站，除非换非标端口再套 CDN
- 搜索引擎抓取、小程序服务端校验、大部分 API 回调会失败
- 搭代理得用 443 以外的端口，或者再套一层 CDN 转发

IRVINE-PRO 更严格，页面写的是“拒绝所有外部探测和扫描”，只有配过白名单或端口转发的设备能访问。安全性上去了，代价是这台机器默认不能被公网随便连。

想建站、跑小程序后端、对外提供 API，住宅 IP 这几档直接跳过。LAX 系列端口全开，同样 2 核 2G 便宜 $60。

👉 [对比 LAX 系列与住宅 IP 系列的年付价](https://sixtynet.net/aff.php?aff=39)

## 按用途对号入座

**个人博客、轻量建站**：LAX-STARTER，$200/年。2 核 2G 跑 WordPress、Typecho、Hugo 够用，5TB 月流量对中小站点是过剩的。

**外贸站、跨境电商后台**：LAX-MICRO，$400/年。4 核 4G、80G、10TB，PHP 和 MySQL 同时跑不会互相挤内存，后台传图、导订单表也扛得住。

**API 服务、爬虫节点**：从 LAX-STARTER 起步，出口流量吃紧再升 LAX-MICRO。这类业务最看重流量和端口带宽，内存不是瓶颈。

**流媒体解锁、账号环境、广告投放**：Residential-STARTER $260/年。要中国方向回程更稳，加 $90 上 IRVINE-PRO-STARTER，页面明确标了 AS9929。

**AI 工具中转、ChatGPT API 代理**：LAX-STARTER 就够。这类用途要的是稳定出口和干净的 IP，住宅 IP 不是必要条件，80/443 封锁反而添麻烦。

**大流量下载、视频中转、备份**：LAX-MEDIUM $800/年给 20TB 和 10Gbps；只缺存储不缺 CPU 的话，LAX-Storage-500G 用同样的 $400 年费换来 500G RAID10 和 10TB 流量，比 LAX-MICRO 的 80G 划算得多。

**BGP 广播、多线接入**：China Unicom-Premium，$2,500/年。100M 基础带宽、3 倍突发、95th 计费、免费 BGP session，这套配置面向有 AS 号、要自己播 IP 的人，个人站长用不上。

## 年付、续费和退款：几个写在页面角落的条件

**全部年繳，页面没有月付报价**。这意味着最低一次性支出 $200，最高 $2,500。对比按月付费的商家，试错成本高出一截。

**折扣幅度 13%–17%，续费价没写**。年付折扣是首期优惠还是长期价格，官网页面上找不到说明。打算长期用，下单前问清楚续费是不是同价。

**IRVINE-PRO 的退款只退到网站余额**。页面原文写的是退款仅对网站余额有效，不是退回原支付渠道。这一档年付 $350 起，条款值得先看清楚。

**China Unicom-Premium 按 95th 计费**。100M 基础带宽、3 倍突发，超出部分按 95th percentile 统计。跑满带宽的业务要先算这笔账，它和“不限流量”是两回事。

**性能不是这条产品线的卖点**。第三方测评对 Cox 住宅 IP 机型的评价是 CPU 性能不错、I/O 偏弱，实测 I/O 大约 188MB/s。跑数据库、编译这类吃磁盘的任务，先按这个水平预期。

👉 [下单前核对 IRVINE-PRO 的年付价与退款条款](https://sixtynet.net/aff.php?aff=39)

## 同周期横比：$200/年 在洛杉矶能买到什么

各家标价周期不一样，直接比数字会得出错误结论。把月付换算成年、年付换算成月，再放到一张表里看：

| 商家与套餐 | 配置 | 端口、流量 | 标价 | 折合月均 |
| --- | --- | --- | --- | --- |
| SixtyNet LAX-STARTER | 2 核 2G / 40G NVMe | 2Gbps / 5TB + DDoS | $200/年 | 约 $16.7 |
| SixtyNet Residential-STARTER | 2 核 2G / 40G NVMe | 2Gbps / 5TB + 住宅 IP | $260/年 | 约 $21.7 |
| SixtyNet IRVINE-PRO-STARTER | 2 核 2G / 40G NVMe | 2Gbps / 5TB + 住宅 IP + AS9929 | $350/年 | 约 $29.2 |
| ProwHost Starter | 1 核 1G / 25G NVMe | 1TB | $13.99/月 | $13.99（年约 $168） |
| OliveVPS Starter | 1 核 1G / 25G NVMe | 1Gbps / 1TB | $3.99/月 | $3.99（年约 $48） |
| is\*hosting Lite | 1 核 1G / 20G | 2TB | $5.94/月（年付口径） | 约 $5.94 |
| ZgoCloud 国际线 | 1 核 1G / 20G NVMe | 1Gbps / 2TB | $15/年（特价） | 约 $1.25 |
| ZgoCloud 国际线 | 2 核 2G / 40G NVMe | 1Gbps / 4TB | $25/年（特价） | 约 $2.1 |
| 野草云 USA-AMD-1C1G | 1 核 1G / 15G | 500Mbps / 1TB + 20GB DDoS | ¥26/月 | ¥26（年约 ¥312） |
| 野草云 USA-AMD-2C4G | 2 核 4G / 30G | 500Mbps / 2TB | ¥43/月 | ¥43（年约 ¥516） |

美元和人民币分开列，没做汇率换算，汇率随时在动，同币种内部对比才有意义。

换算完，SixtyNet 在这张表里是最贵的一档。同样 2 核 2G，ZgoCloud 国际线路年付 $25 就能拿到（特价），野草云 1 核 1G 月付 ¥26，OliveVPS 1 核 1G 月付 $3.99、年付不到 $48。

SixtyNet 贵在三样东西：2Gbps 起步的端口和 5TB 起的月流量、DDoS 防护、以及住宅 IP 这条产品线。前两样在纯建站场景里是浪费，一个日 PV 几千的博客用不到 2Gbps 端口，也用不上 DDoS 清洗。第三样别的家基本不做，愿意为住宅 IP 付溢价的人，选择本来就不多。

反过来说，如果你的需求就是建站、跑个小 API、做个中转，ZgoCloud 或野草云更省钱，没必要为用不上的带宽和 IP 属性多付一百多美元。

## 最后怎么定

按需求走三条路：

- 要一台能建站、能跑服务、端口齐全的洛杉矶机器 → **LAX-STARTER，$200/年**
- 业务依赖“住宅 IP”这个属性（流媒体、账号、投放） → **Residential-STARTER $260/年**，或加 $90 上 IRVINE-PRO-STARTER 拿 AS9929
- 要自己播 IP、按 95th 计费跑带宽 → **China Unicom-Premium $2,500/年**

下单前确认两件事。一是当前批次的测试 IP 和回程路由，住宅 IP 的上游运营商会换，页面上的 AS9929 标注和到手机器的实际路由要分开核。二是 25 端口能不能用，洛杉矶不少商家默认封 25 端口，有的要交保证金才放通，SixtyNet 页面上没写这条，有发信需求必须先问客服。

👉 [去 SixtyNet 看洛杉矶各系列当前年付价](https://sixtynet.net/aff.php?aff=39)
