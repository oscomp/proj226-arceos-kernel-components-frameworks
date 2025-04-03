# proj226-tangram-kernel-components-and-frameworks
# 象七巧板一样灵活组合的操作系统模块和框架--tangram-kernel-components-frameworks
- [唐图(rCoreOS)开源社区](https://github.com/rcore-os)

本社区起源于2017年底，清华大学计算机系操作系统课开始探索基于Rust语言的OS实验，并在2018年推出了教学操作系统rCore，并放到了github上。后续逐步开展科研探索，形成了rCore-Tutorial、rcore-in-single-workspace、zCore, ArceOS等一系列的教学科研操作系统。在对这些操作系统进行教学和研发的过程中，我们在进一步思考，能否以单个内核组件为可独立存在并运行的基本单元，并把这些单元组合在一起，形成不同形态和功能的操作系统内核。现在我们正在开发各种内核组件，并尝试组合出arceos、starry、axvisor等异构内核，欢迎大家一起加入我们这个社区！

### 支持单位 
- [唐图(rCoreOS)开源社区](https://github.com/rcore-os)
- [开源操作系统训练营](https://opencamp.cn/os2edu/camp/2025spring)
- 清华大学计算机系操作系统课题组
### 项目描述
基于组件化设计的思路，用Rust语言的丰富语言特征，设计实现不同功能的独立操作系统内核模块和操作系统框架。帮助内核开发者像开发应用那样，灵活组合出不同特征/形态/架构的操作系统内核。

### 所属赛道
2025全国大学生操作系统比赛的“OS功能挑战”赛道

### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生（2025年春季学期或之后毕业的大一~大四的本科生或研究生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

- 陈渝 github id: chyyuu   email：yuchenATtsinghua.edu.cn
- 石磊 github id: xyongcn  email: xyong@tsinghua.edu.cn

### 难度

初等--中等--高等

### 特征

- 熟悉操作系统/计算机组成原理等基本概念
- 熟悉Rust语言


### 参考资源
#### 面向教学
- [rCore Tutorial Kernel：教学用内核组件化初步探索](https://github.com/rcore-os/rCore-Tutorial-in-single-workspace)
- [rCore Tutorial Kernel：教学用内核组件化进一步探索](https://github.com/crates-rcore-in-single-workspace)
- [多型态组件化操作系统：教学用内核组件化再进一步探索](https://opencamp.cn/os2edu/camp/2024fall/stage/3)
#### 面向科研 
- [unikernel形态的组件化内核ArceOS kernel](https://github.com/oscomp/arceos)
- [宏内核形态的组件化内核Starry-next kernel](https://github.com/oscomp/stary-next)
- [Hypervisor形态的组件化hypervisor](https://github.com/arceos-hypervisor/axvisor)
- [开源内核组件汇聚中心](https://github.com/kern-crates)
  
### License

- GPL-3.0 
- Apache-2.0



## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标
如果是与OS无关的kernel component，要求能建立为github上的一个独立仓库（比赛官网也要有同样的仓库），能独立形成crate（能提交到crates.io），能独立测试和与OS合并测试。

### 具体内容
基于在唐图社区（包括位于github上的rcore-os，arceos, starry-next，arceos-hypervisor，kern-crates等）的Rust内核组件和组件框架进行改进，或进一步设计实现新的内核组件和内核组件框架，形成可灵活组合的各种异构形态和功能的内核。具体要求如下所示（可在下面不同形态的内核中选择一个或多个）：
- 改进或创新并组合组件形成支持openKylin Linux应用的组件化宏内核，可运行全国大学生操作系统内核实现赛道的Linux应用测试用例；
- 改进或创新并组合组件形成支持openKylin Linux应用的组件化微内核，可运行全国大学生操作系统内核实现赛道的Linux应用测试用例；
- 改进或创新并组合组件形成支持运行多个内核的组件化虚拟化软件，可运行支持Linux应用的组件化宏内核，以及支持Linux应用的组件化微内核等；
- 改进或创新并组合组件形成各种新颖功能或创新功能的组件化内核，如支持硬件新特性、故障隔离、动态加载和热升级能力等。

### 评价指标
#### 功能完整性（60%）
- 改进或创新并组合组件形成的宏内核或微内核形态可运行全国大学生操作系统内核实现赛道初赛的Linux应用测试用例，以通过的测例数量为功能完整性评价指标；改进或创新并组合组件形成的虚拟化软件可运行Guest Mode的Linux内核和某个其他内核，以支持的虚拟化功能数量为功能完整性评价指标；改进或创新并组合组件形成新型组件化内核的新颖功能，有实际测例说明组件和内核的创新性，以创新性的可量化指标为功能完整性评价指标；（100分）
#### 应用效果（20%）
- 支持x86-64/aarch64/Risc-V64/LoongArch64 QEMU-9.2+模拟环境或物理环境中的一种处理器上运行；（40分）
- 有额外的测试用例能展示组件或组件化内核的功能、性能、安全等特征；（40分）
- 运行效果可重现；（20分）
#### 代码规范 （10%）
- 基于Rust 2024版本进行开发；（40分）
- 代码结构清晰、符合开源社区规范、可维护性高；（20分）
- 能通过Rust的代码规范性检查；（40分）
#### 文档质量（10%）
- 文档包含设计文档、安装部署说明、测试分析报告；（50分）
- 文档条例清晰、撰写规范；（50分）


## 备注

鼓励在唐图开源社区与大家多交流。
