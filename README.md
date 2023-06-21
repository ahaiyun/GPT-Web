<div align="center">

![ChatGPT Web](./src/assets/openai.svg)

# ChatGPT-Web

基于79E/ChatGpt-Web项目二次开发的商业化 ChatGPT-Web。

</div>

## 演示站点

- 演示地址：[Web 演示](https://gptchat.hyjl.tech/)
- 后台地址：https://gptchat.hyjl.tech/admin
- 管理账号：jl@admin.com
- 管理密码：admin123456

如需帮助请提交 [Issues](https://github.com/ahaiyun/GPT-Web/tree/master/issues) 时留下联系方式。

### 页面截图

![页面截图1](https://files.catbox.moe/tp963e.png)
![页面截图![1686740335-46f959d0eb26a25](https://github.com/ahaiyun/GPT-Web/assets/105539354/0a859300-085a-4b13-9c65-e8488326872f)
2](https://files.catbox.moe/y5avbx.png)
![1686740427-24a471501b79e1f](https://github.com/ahaiyun/GPT-Web/assets/105539354/47ffdfb3-8fb8-439d-9b0e-4e355053d273)
![1686740458-0db52d5a933bb84](https://github.com/ahaiyun/GPT-Web/assets/105539354/e0e201ae-e74c-45a7-9333-c695655d426d)
![1686740520-2d10f2bc38b6529](https://github.com/ahaiyun/GPT-Web/assets/105539354/bc02ed08-f6b9-476c-9a1b-e598606292ed)
![1686740521-9c9b4fe2faf8df2](https://github.com/ahaiyun/GPT-Web/assets/105539354/eb2e6516-2e37-4d03-8502-18fb398754e4)

### 欢迎加入群聊：
![屏幕截图 2023-06-21 213643](https://github.com/ahaiyun/GPT-Web/assets/105539354/54246107-208e-4197-a53a-327444b4d746)

## 主要功能

- 后台管理系统，登陆注册、商品管理、订单管理、卡密管理(二级分销)、用户管理
- 支持微信支付宝官方支付、易支付、支持用户付费套餐设置
- 精心设计的 UI，响应式设计
- 极快的首屏加载速度（~100kb）
- 支持 DALL·E 模型绘画，GPT3.5和4.0（接口可选官方和第三方API自定义设置）等应用
- 海量的内置 prompt 列表，来自[中文](https://github.com/PlexPt/awesome-chatgpt-prompts-zh)和[英文](https://github.com/f/awesome-chatgpt-prompts)
- 一键导出聊天记录
- 支持第三方API自定义设置（如：[openAI](https://api.openai.com) / [API2D](https://api2d.com/r/192767)）

## 运行环境

- Node 版本: `node` 需要 `^16 || ^18 || ^19` 版本（node >= 16.19.0），可以使用 nvm 管理本地多个 node 版本。
- ```
查看 node 版本:
node -v

查看 npm 版本:
npm -v

查看 yarn 版本:
yarn -v


- 数据库: MYSQL + Redis
- 两个域名: 一个用作前端，一个用作后端跳转

### 前端

**环境变量**


1. 安装 nodejs 和 yarn具体细节请询问 ChatGPT
2. 执行 `yarn install` 即可
3. web项目开发 `yarn dev:web`
4. 服务端项目开发 `yarn dev`
5. 打包项目 `yarn build`


### 后端

导入 MySQL 数据库文件： `sql/chatgpt.sql`

在 `server/config/index.js` 中修改 `后端端口` `数据库` `邮箱` 等配置

```
##安装 pm2 管理器
sudo npm install pm2 -g

cd server

#### 启动进程
pm2 start index.js --name chatweb --watch
```
新建一个网站，ssl验证后，反向代理 `http://127.0.0.1:3200`(可在后端配置中自行修改端口)

## 🎯 部署
> 直接将`WEB`项目打包好的 `dist` 目录上传到服务器即可。注意服务器IP地址位置！

### Vercel 部署

如果你将其托管在自己的 Vercel 服务器上，可点击 deploy 按钮来开始你的部署！

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/ahaiyun/GPT-Web/tree/master)

### 服务器部署


## `Fork`项目
git clone https://github.com/ahaiyun/GPT-Web.git

## 安装依赖（注意先安装好 node 及 yarn）
以及 yarn）
yarn install

## 打包
yarn build

将打包好的 dist 目录上传到服务器，将网站目录指向 dist 文件夹即可


需额外在伪静态中添加
```
location / {
  try_files $uri $uri/ /index.html;
}
```

## 更多

关于 `node` `yarn` `pm2` 以及 Vercle 的一些设置可以自行搜索或向[GPT](https://ai.ligthai.io) 提问

## 贡献者
感谢项目原作者 [79E](https://github.com/79E) 以及所有的 [项目贡献者](https://github.com/ahaiyun/GPT-Web/tree/master/graphs/contributors)

## 开源协议
[![License MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://github.com/vastxie/ChatGpt-Web/blob/master/license)
