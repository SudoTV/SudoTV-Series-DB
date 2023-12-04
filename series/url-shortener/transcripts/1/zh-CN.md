---
locale: zh-CN
---

Hello 大家好，欢迎来到本期小教程。从今天开始，我们会使用 Express 和 React 一起完成一个短链接生成器。这套教程适合想尝试一下的新手，有一点点了解但是没有项目经验的学生，甚至没有尝试过现代网页开发的从业者。我们会使用 NodeJS 来完成后端的工作，使用 React 来完成前端的工作。如果你一会感觉到很疑惑。你可以看看我之前的视频，或者访问 https//sudo.tv/series/url-shortener/episode/1/learn-the-basics 查看我们推荐的文章。

## 创建项目

Express 的项目非常简单，我们不需要任何步骤，只需要安装 Express 并且创建一个文件夹就可以了。我们可以使用 `npm init` 来创建一个新的项目，然后使用 `npm install express` 来安装 Express。我们可以在 `index.js` 中写入以下代码：

```js
const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(3000, () => {
  console.log('Example app listening on port 3000!');
});
```

## 运行项目

我们可以使用 `node index.js` 来运行项目，然后在浏览器中访问 `http://localhost:3000` 来查看我们的项目。如果你看到了 `Hello World!`，那么恭喜你，你已经成功运行了你的第一个 Express 项目。

之所以我们能够看到 `Hello World!`，是因为我们在 `index.js` 中写入了 `app.get('/', (req, res) => { res.send('Hello World!'); });`。这段代码的意思是，当我们访问 `http://localhost:3000` 的时候，我们会返回 `Hello World!`。

我们需要引入一个概念，HTTP 请求，HTTP 请求是我们在浏览器中访问网页的时候，浏览器向服务器发送的请求。这个请求包含了很多信息，比如我们访问的网址，我们的浏览器版本，我们的操作系统，我们的 IP 地址等等。我们可以在 `app.get('/', (req, res) => { res.send('Hello World!'); });` 中看到，我们的 `app.get` 接受两个参数，第一个参数是我们的网址，第二个参数是一个函数，这个函数接受两个参数，第一个参数是我们的请求，第二个参数是我们的响应。我们可以在这个函数中，根据我们的请求，来返回不同的响应。比如我们可以根据我们的请求，返回不同的网页，或者返回不同的数据。

## 短链接跳转

基于我们这里说的，当浏览器访问 `http://localhost:3000` 的时候，我希望我们的服务器能把用户跳转到 `https://sudo.tv`。我们可以在 `index.js` 中写入以下代码：

```js
const express = require('express');

const app = express();

app.get('/', (req, res) => {
  res.redirect('https://sudo.tv');
});

app.listen(3000, () => {
  console.log('Example app listening on port 3000!');
});
```

我们可以看到，我们使用了 `res.redirect('https://sudo.tv');` 来跳转用户。我们可以在浏览器中访问 `http://localhost:3000` 来查看我们的项目。如果你看到了 `https://sudo.tv`，那么恭喜你，你已经成功跳转了用户。

## 下一集

在下一集中，我们会继续学习 Express，我们会学习如何使用 Express 来处理 POST 请求。但是在这之前你可以访问 https://sudo.tv/series/url-shortener/episode/1/deep-dive，对于每一集视频，你可以在这里找到深入学习需要的文章和练习。
