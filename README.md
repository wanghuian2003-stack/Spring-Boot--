# 🟦 Detroit: Become Human (Web Ver) | 底特律：变人 (网页版)

![License](https://img.shields.io/badge/license-MIT-blue) ![Java](https://img.shields.io/badge/Java-17-orange) ![SpringBoot](https://img.shields.io/badge/SpringBoot-3.0-green)

这是一个基于 **Spring Boot** 开发的文字冒险游戏 (AVG) 引擎，复刻了《底特律：变人》的核心剧情。项目包含复杂的多分支叙事系统、好感度判定、QTE 模拟以及邮件验证码登录系统。

## 🎮 功能特性 (Features)
* **多分支剧情系统**：基于数据库的节点跳转，每一个选择都会改变故事走向。
* **蝴蝶效应机制**：内置好感度（汉克、爱丽丝）、舆论值、软件不稳定度等隐藏数值，影响最终结局。
* **多主角视角**：支持康纳、卡拉、马库斯三线叙事切换。
* **用户系统**：支持账号密码注册/登录，以及**邮箱验证码免密登录**（自动注册）。
* **存档系统**：自动保存玩家当前进度和所有决策变量。

## 🛠️ 技术栈 (Tech Stack)
* **后端**：Java 17, Spring Boot 3.x, Spring Data JPA
* **数据库**：MySQL 8.0
* **前端**：JSP, JSTL, CSS3 (响应式设计), JavaScript (Fetch API)
* **工具**：Maven, Git

## 💻 运行环境 (Requirements)
在运行本项目前，请确保您的环境满足以下要求：
1.  **JDK**：17 或更高版本
2.  **MySQL**：8.0+
3.  **Maven**：3.6+

## 🚀 快速开始 (Quick Start)

### 1. 数据库配置
1.  在 MySQL 中创建一个名为 `detroit_db` 的数据库。
2.  导入项目根目录下的 `detroit_backup.sql` 文件（包含完整剧情数据）。
3.  修改 `src/main/resources/application.yml` 中的数据库账号密码：
    ```yaml
    spring:
      datasource:
        username: your_username
        password: your_password
    ```

### 2. 邮件服务配置 (可选)
如果需要测试邮箱登录功能，请在 `application.yml` 中配置 SMTP 服务（如 QQ 邮箱授权码）。

### 3. 启动项目
```bash
mvn spring-boot:run
```
访问：`http://localhost:8080`

## 📂 项目结构
* `controller`: 处理 Web 请求与页面跳转
* `model`: 定义 User, StoryNode, GameArchive 等实体
* `repository`: 数据库访问层 (JPA)
* `src/main/webapp`: 前端 JSP 页面与静态资源

## 📜 声明
本项目仅用于学习 Spring Boot 开发，剧情文本与设定版权归 Quantic Dream 所有。


<img width="1026" height="249" alt="image" src="https://github.com/user-attachments/assets/2b466960-078b-4c11-851c-35248f3e9b63" />

