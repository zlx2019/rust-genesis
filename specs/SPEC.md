# Project Name

这是一个什么项目。



## 1.项目背景(Why)
- 当前存在的问题：
- 为什么需要这个项目：
- 适用场景：

> 说明性即可，不需要情绪化描述。

## 2.项目目标(What)




## 3.核心约束（Constraints）
用于防止 AI 过度设计或跑偏，这是非常重要的一节。
- 编程语言：Rust(stable)
- 是否允许异步：使用 Tokio(async。
- 数据存储：内存存储(不使用数据库)
- 优先级: 可读性 > 扩展性 > 性能。
- 尽可能避免`Clone`频繁分配内存。
- 目标用户(个人 / 团队 / 生产环境): 生产环境。

## 4. 总体架构设计(High-level Design)
### 4.1 项目结构
```
src/
├── main.rs # 程序入口
├── config/ # 配置相关
├── app/ # 应用层 / 用例层
├── domain/ # 领域模型（尽量纯粹）
├── infra/ # 基础设施(日志、IO、存储等)
└── utils/ # 通用工具
```

### 4.2 项目职责
- main：初始化应用并启动程序。
- config：配置相关。
- app:
- domain:
- infra:
- utils:
每个模块只写「做什么」，不要写「怎么做」。

## 5.功能需求（Functional Requirements）
### 5.1 功能一
- 功能描述:
- 输入:
- 输出:
- 异常情况:

### 5.2 功能二
- 功能描述:
- 输入:
- 输出:
- 异常情况:

功能需求优先使用列表和场景，而不是长段落。



## 6.数据模型/接口设计（Data & API）
### 6.1 核心数据结构
```rust
// 示例：配置结构体
pub struct AppConfig {
    pub env: String,
    pub log_level: String,
}
```
### 6.2 核心接口定义
```rust
pub trait Service {
    fn execute(&self) -> Result<(), ServiceError>;
}
```

### 7.代码规范与风格

- 公共结构体和枚举必须添加 doc 注释
- 不使用 `unwrap()`（测试代码除外）
- 所有业务错误使用 `Result`
- 模块对外接口尽量使用 trait
- 使用 Rust 标准命名规范
- 日志 / 错误的基本格式：


### 8.示例代码
这是 AI 学习你风格的关键部分。
```rust
/// 示例函数：加载配置
pub fn load_config() -> Result<AppConfig, ConfigError> {
// 示例实现逻辑
Ok(AppConfig {
    env: "dev".to_string(),
    log_level: "info".to_string(),
})
}
```
示例说明:
- 函数保持简短
- 错误显式返回
- 不隐藏关键逻辑

### 9.非目标
明确声明「不会做什么」，防止 AI 自作主张。
- 不支持:
- 不考虑:
- 明确排除的场景:

### 10.与我的协作方式
说明你希望 AI 如何参与这个项目。
- 每次只实现一个模块
- 实现前先给出设计说明
- 不确定的地方优先提问
- 所有实现必须遵守本需求文档

### 11.迭代记录(Changelog)

```
v0.1  初始化项目需求文档
v0.2  补充配置模块与日志规范
```

> 建议长期维护这一节，作为 AI 的“长期记忆”。

