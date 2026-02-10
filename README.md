# auto_日本游戏机   自动续期脚本


## 1、你需要在仓库 Settings → Secrets and variables → Actions → Secrets 里新增：

- XSERVER_EMAIL

- XSERVER_PASSWORD

- TELEGRAM_BOT_TOKEN（可选）

- TELEGRAM_CHAT_ID（可选）


## 2、开放自动写time.txt的文件权限。
### 这个主要是用于规避github 默认60天的仓库代码没有任何变动就会自动给你发邮件并且自动禁用action的定时任务。

GITHUB_TOKEN 不用你手动创建 —— 只要你的 workflow 在 GitHub Actions 里跑起来，GitHub 会自动为每次运行生成一个临时的 secrets.GITHUB_TOKEN，在 workflow 里直接用就行（你已经在用 ${{ secrets.GITHUB_TOKEN }} 了）。

### 你需要做的通常是 给它权限、以及确认 checkout 会把它用在 push 上。

1) 你需要设置的地方：给它写权限

到仓库：

### Settings → Actions → General → Workflow permissions

选择：

✅ Read and write permissions

然后保存

## 3、关闭网站里的账号敏感通知。
3.1） 打开小日子游戏机网页登录地址进行登录

<img width="500" height="622" alt="CleanShot 2026-02-10 at 08 07 11" src="https://github.com/user-attachments/assets/8766e4cd-fbb1-4fb5-a07f-290f6aaea611" />


<img width="702" height="462" alt="CleanShot 2026-02-10 at 08 10 04" src="https://github.com/user-attachments/assets/33f2e9d3-0ba5-40e8-bbdb-6d106d2c7d42" />

<img width="1096" height="270" alt="CleanShot 2026-02-10 at 08 14 08" src="https://github.com/user-attachments/assets/42b41c6c-ccb0-4213-9660-cbda2f4908fa" />



## 4、修改定时任务执行时间。
### main.yml里面修改你的定时任务的执行时间（建议根据你自己下面的到期时间去调整定时。）

<img width="581" height="105" alt="CleanShot 2026-02-10 at 08 15 53" src="https://github.com/user-attachments/assets/c5ff16ab-842b-48b0-a09b-f2137f199f4c" />













