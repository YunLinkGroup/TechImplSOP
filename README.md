# TechImplSOP
技术实施 SOP















| 对比维度           | KVM                              | VMware vSphere                         | OpenStack                             |
| ------------------ | -------------------------------- | -------------------------------------- | ------------------------------------- |
| 基本定位           | 开源的 Type-1 Hypervisor         | 商用的虚拟化解决方案套件               | 开源的云计算管理平台（IaaS）          |
| 与 KVM 关系        | 自身                             | 竞争关系                               | 通常以 KVM 为默认 Hypervisor          |
| 许可证与费用       | GPL 开源，免费                   | 商用许可证，按 CPU 插槽和功能收费      | Apache 2.0 开源，免费                 |
| 单节点性能         | 接近原生                         | 接近原生，IO 路径经过深度优化          | 取决于底层 Hypervisor（通常是 KVM）   |
| 热迁移             | 支持（需共享存储和配置）         | vMotion 开箱即用，支持跨集群迁移       | 支持（依赖底层 Hypervisor 的能力）    |
| 高可用（HA）       | 需要额外配置（如 Pacemaker）     | 内置 HA、FT、DRS                       | 需要额外配置或商业发行版支持          |
| 多租户与自服务     | 本身不支持，需要云管平台         | 需要额外购买 vRealize 组件             | 内置 API 和控制面板，天然支持         |
| 最大集群规模       | 数十至数百节点（使用 oVirt）     | 数千节点（受 vCenter 限制）            | 上千节点（可通过 Cell 分区扩展）      |
| 图形化管理界面     | virt-manager、oVirt、Proxmox     | vCenter 统一门户                       | Horizon（功能有限，更多使用 CLI/API） |
| 学习曲线           | 中等（需要 Linux 和网络基础）    | 低（图形化界面，Windows 风格）         | 高（架构复杂，涉及多组件）            |
| 商业支持           | Red Hat RHV、SUSE、Canonical     | VMware 官方及众多集成商                | Red Hat、Mirantis、华为等发行版       |
| 社区活跃度         | 高（Linux 内核社区）             | 中等（VMware 官方主导）                | 高（由基金会和各大厂商共同维护）      |
| 与云原生生态亲和度 | 极佳（K8s 云厂商底层）           | 一般（需要 Tanzu 集成）                | 可并存（K8s-on-OpenStack 方案）       |
| 安全合规认证       | 可配合 CIS、FedRAMP 等           | 大量金融、医疗合规案例                 | 需要商业发行版补齐（如 FIPS、等保）   |
| 典型使用场景       | 开发测试、K8s 实验床、成本敏感型 | 生产关键业务、Windows 虚机多、预算充足 | 大型数据中心、多租户私有云、混合云    |





虚拟化，k8s、docker

各种组件，mysql、redis、es、kafka、rabbitmq、prometheus、alertmanager、grafana、postgresql、kong、consul、nacos

gitlab、镜像仓库



