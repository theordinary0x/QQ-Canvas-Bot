# QQ-Canvas-Bot
A QQ bot send Canvas message and assignment to users.

# TODO List

- [ ] **初始化 Python 项目 / Initialize the Python project**
  建立项目结构、依赖管理与配置文件(技术栈:Python)/ Set up project structure, dependency management, and configuration (stack: Python)
- [ ] **接入 QQ 机器人平台 / Integrate the QQ bot platform**
  在腾讯平台注册机器人并获取接入凭证;安装并配置 NoneBot2 / Register the bot on the Tencent platform and obtain credentials; install and configure NoneBot2
- [ ] **验证 Canvas API 访问 / Verify Canvas API access**
  使用 CanvasAPI 库 + Access Token,测试读取课程、作业、公告与文件 / Use the CanvasAPI library with an access token to test reading courses, assignments, announcements, and files
- [ ] **设计数据存储 / Design data storage**
  保存 QQ–Canvas 账号绑定关系、作业提交状态、已发送提醒记录 / Persist QQ–Canvas account bindings, assignment submission states, and sent-reminder logs
- [ ] **设计 Token 安全方案 / Design access-token security**
  Access Token 授予程序读取学生信息的权限,必须妥善保管(加密存储、不落地日志)/ The access token grants access to student data and must be kept secure (encrypted storage, never logged)

---

- [ ] **账号绑定 / Account connection**
  实现学生 QQ 账号与 Canvas 账号的绑定流程(Access Token 的提交与验证)/ Implement the flow for students to connect their QQ account to their Canvas account (token submission and validation)
- [ ] **查询引擎 / Query engine**
  通过 Canvas REST API 拉取指定数据(作业、课程文件等)/ Fetch the requested data (assignments, course files, …) through the Canvas REST API
- [ ] **数据处理器 / Data processor**
  校验并整理 Canvas 返回的数据,组织成可读消息 / Check and organize Canvas responses into readable messages
- [ ] **定时轮询器 / Scheduled poller**
  每 3–5 分钟轮询 Canvas,检测变化并自动触发通知流程 / Poll Canvas every 3–5 minutes to detect changes and automatically trigger the notification flow
- [ ] **/deadline 命令 / /deadline command**
  学生发送 `/deadline` 查询未完成作业,回复展示每项任务与剩余时间 / Students type `/deadline` to list unfinished assignments; the reply shows each task and the time remaining
- [ ] **新作业通知 / New-assignment notification**
  检测到新作业时,推送标题、截止时间、提交状态与相关文件 / When a new assignment appears, push its title, deadline, submission status, and related files

---

- [ ] **/files 命令与文件投递 / /files command and file delivery**
  学生发送 `/files` 查找课程资料;小文件直接通过 QQ 发送,大文件提供下载链接 / Students type `/files` to find course materials; send small files directly through QQ and provide download links for larger ones
- [ ] **截止提醒策略 / Deadline reminder policy**
  截止前 24 小时发送首次提醒;剩余 12 小时发送紧急提醒;Canvas 显示已提交后停止提醒 / First reminder 24 hours before the deadline; urgent reminder when 12 hours remain; stop once Canvas shows the work has been submitted
- [ ] **公告通知 / Announcement notifications**
  检测到重要公告(如期中演示安排)时推送 QQ 通知,提醒学生查看 / Push a QQ notification when an important announcement appears (e.g., the midterm presentation arrangement) so students know to check
- [ ] **安静时段 / Quiet hours**
  默认 23:00–08:00 不发送提醒,紧急通知按策略处理 / Default quiet hours 11 p.m.–8 a.m.; suppress reminders, with a policy for urgent ones

---

- [ ] **完善安静时段 / Refine quiet hours**
  支持更细的策略与个性化设置 / Support finer policies and per-user customization
- [ ] **多用户扩展 / Expand to more users**
  提升并发轮询与消息吞吐的可靠性,完成部署上线 / Improve concurrent polling and message throughput; finish deployment
- [ ] **验证项目价值 / Validate the project's value**
  度量学生查看课程页面的时间是否减少、错过截止的情况是否降低 / Measure whether students spend less time checking course pages and miss fewer deadlines

---

- [ ] **作业提交功能 / Assignment submission**
  允许通过机器人提交作业;因会更改 Canvas 上的信息,需更谨慎的测试 / Allow submitting assignments via the bot; requires more careful testing because it changes information on Canvas
