# parkingsmart-doc

## Git

### 协作管理
* 每次打开 IDE 的时候先 Pull 最新代码到本地
* 每次 Commit 之前先 Pull 最新代码到本地
* 在完成完整的部分功能前提下, 小步提交
* 不要在项目不能正常运行的情况下提交代码

### Branch
* **master:** 线上生产环境
* **test:** 线上测试环境
* **dev:** 本地开发环境

### Commit message
* 统一使用英文
* 格式为 `[{type}] {desc}`, 如 `[feat] add the page for user management`

#### Type:
* init: 初始化项目
* feat：新功能（feature）
* fix：修补bug
* docs：文档（documentation）
* style： 格式（不影响代码运行的变动）
* refactor：重构（即不是新增功能，也不是修改bug的代码变动）
* test：增加测试
* chore：构建过程或辅助工具的变动