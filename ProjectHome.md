# 名称由来 #
鼹鼠 mole，善于挖打洞地道。为了避免和另一个项目 mole 命名冲突，用 MoleTunnel。

# 目前状态 #
  1. 人力组织
  1. 结构设计
  1. 技术说明文档撰写

# 技术方案 #
一个简单的 GUI 来集成 freecaps+stunnel 作为客户端，服务端 3proxy + stunnel。
实现的语言用 C++，java, python 都可以。

让非专业人士能非常容易地通过朋友的计算机上网。

可以通过 im 社交网络信任关系给予授权，显示服务器状态信息。
自动调用 im 传递服务器信息，比如服务器的外部地址，用户名，密码之类。
因为要能突破 nat 的限制啊。尤其服务器端。
经由 im 信道触发服务器的开启和关闭，对特定用户授权。全部自动完成。
im 是一个沟通的 bootstrap 渠道，起到名服务的作用。
先基于 skype 做，可以先以 skype plugin 的方式安装。
以后扩展到其他的 IM，如 msn, qq, gtalk。
基本配置信息可以通过 IM，也可以通过 email 传递。

利用 IM 这个天然的社会工程信任安全模式的基础。这种分布式的代理，是绝对无法封锁的。
类似 psiphon 但是提供更通用的 socks5+ssl 通道。墙内的装鼹鼠服务器也可以让墙外的进入墙内作测试。
或者突破双向关键词封锁。

通过 upnp 打开路由。要几乎 0 配置。

socks5 proxy 我现在选 3proxy。
sockscap32 不是 freeware。freecap 似乎和 ie8, chrome 不兼容，firefox 可以。
因为需要远程 dns 解析，必须支持 socks5 代理，还支持 udp proxy。

高级目标：可以通过 port forwarding 在远程实现服务端口接听。也就是说，可以让墙外的服务器，在墙内提供分布式的服务。

# 开发文档 #
  1. [Guidelines](Guidelines.md) 开发者指南
  1. [ReferenceDevelopmentDocuments](ReferenceDevelopmentDocuments.md) 参考文档