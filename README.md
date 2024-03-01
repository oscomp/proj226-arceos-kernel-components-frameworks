# proj226-arceos-kernel-components-frameworks
# 灵活组合的操作系统模块和框架--ArceOS-kernel-components-frameworks
- [想法来源：基于泛型独立组件构建各种领域OS](https://github.com/chyyuu/thoughts/blob/main/tangram-oskits.md)
- [ArceOS: 组件化操作系统的初步探索](https://learningos.github.io/os-lectures/oslabs/biglabs.html#2)
- [ArceOS源码仓库](https://github.com/rcore-os/arceos)
- [rCore OS开源社区](https://github.com/rcore-os/)
- [LearningOS开源社区](https://github.com/learningos)

### 支持单位 
清华大学

### 项目描述
基于组件化设计的思路，用Rust语言的丰富语言特征，设计实现不同功能的独立操作系统内核模块和操作系统框架，可形成不同特征/形态/架构的操作系统内核，独立操作系统内核模块可支持不同的操作系统内核。让领域操作系统易于定制/开发/复用。

### 所属赛道
2024全国大学生操作系统比赛的“OS功能挑战”赛道

### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生（2024年春季学期或之后毕业的大一~大四的本科生或研究生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2024全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

- 陈渝 github id: chyyuu   email：yuchenATtsinghua.edu.cn
- 贾越凯 github id：equation314 email: jyk19ATmails.tsinghua.edu.cn
- 石磊 github id: shilei-massclouds email: shi_leiATmassclouds.com
- 杨金博 github id: yfblock email: 321353225@qq.com

### 难度

初等--中等--高等

### 特征

- 熟悉操作系统/计算机组成原理等基本概念
- 熟悉Rust语言
- 能通过[开源操作系统训练营](https://github.com/learningos)的训练



### 参考资源

#### kernel&hypervisor
这是可供参考的OS&Hypervisor，要求参赛者设计的kernel components 能够支持部分（不一定全部）的如下OS&Hypervisor
- [unikernel形态的组件化ArceOS](https://github.com/rcore-os/arceos)
   - [可运行在RISC-V星光二代开发板三的ArceOS](https://github.com/yuoo655/arceos_net/tree/starfive2)
- [基于ArceOS的宏内核形态的组件化Starry kernel](https://github.com/Arceos-monolithic/Starry)
- [宏内核形态的组件化Byeos kernel]( https://www.github.com/yfblock/Byteos)
- [基于ArceOS的微内核形态的组件化os kernel](https://github.com/jhdjames37/arceos)
- [基于ArceOS的Hypervisor形态的组件化hypervisor](https://github.com/arceos-hypervisor/hypercraft)

#### 参考：与OS无关的kernel components
这是部分与OS无关的kernel components，有一些不一定特别完善，供参考，也可进一步改进作为比赛提交成果

- [基于C的ext4 crate](https://github.com/rcore-os/lwext4_rust)
- [基于Rust的ext4 crate](https://github.com/yuoo655/ext4_rs)
- [Rust-based tcpip stack: smoltcp](https://github.com/rcore-os/smoltcp)
- [C-based tcpip stack:lwip](https://github.com/Centaurus99/arceos-lwip)
- [virtio drivers](https://github.com/rcore-os/virtio-drivers)
- [e1000 NIC driver](https://github.com/rcore-os/e1000-driver)
- [Cadence Macb ethernet driver on Sifive fu740 board](https://github.com/rcore-os/cadence-macb-driver)
- [RISC-V星光二代开发板的网卡驱动](https://github.com/yuoo655/visionfive2_net_driver)
- [nvme driver](https://github.com/rcore-os/nvme_driver)
- [isomorphic_drivers](https://github.com/rcore-os/isomorphic_drivers)
- [os scheduler](https://github.com/131131yhx/arceos)
- [os memory malloc subsystem](https://github.com/rcore-os/mem_malloc_subsystem)

### License

- GPL-3.0 
- Apache-2.0



## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标
如果是与OS无关的kernel component，要求能建立为github上的一个独立仓库（比赛官网也要有同样的仓库），能独立形成crate（能提交到crates.io），能独立测试和与OS合并测试。

评价项目完成情况的一个重要指标是被其他仓库的引用数量（代表有proj用了这个crate）和fork数量、Star数量，以及使用和设计实现文档等。virtio-drivers crate的引用数量和fork数量、Star数量是一个好评价的参考。

- 改进已有的与OS无关或相关的kernel component
- 增加新的与OS无关或相关的kernel component
- 改进或增加OS内核框架，形成新的OS
- 一些kernel components具体内容
  - 算法：调度、内存分配、...
  - 驱动：物理网卡、SD 卡、virtio GPU、各种外设驱动...
  - 文件系统：各种嵌入式文件系统
  - 硬件相关层：支持x64/ARM/RISC-V/LoogArch（龙芯）架构的HAL

## 备注

鼓励在各种项目中重用与OS无关的内核组件和框架。
