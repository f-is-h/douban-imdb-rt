# 豆b番——豆瓣电影显示IMDb和烂番茄评分

<div align="center">
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/alternatives/icon_original.png" width="128" height="128"/>
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/equals.png" width="78" height="78" style="margin: 20px 20px;"/>
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/douban.png" width="128" height="128"/>
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/plus.png" width="78" height="78" style="margin: 20px 20px;"/>
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/imdb.png" width="128" height="128"/>
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/plus.png" width="78" height="78" style="margin: 20px 20px; "/>
<img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/rottentomatoes.png" width="128" height="128"/>
</div>

## 效果展示

![效果展示](https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/screenshots/v1/preview.png)

## 功能
- 显示IMDb评分和评分人数
- 显示烂番茄专业评分和观众评分
- 点击评分可跳转到对应网站查看详情

## 安装
1. 首先需要安装 [Tampermonkey](https://www.tampermonkey.net/) 等浏览器扩展
2. 然后点击 [这里](https://greasyfork.org/zh-CN/scripts/527823-%E8%B1%86%E7%93%A3%E7%94%B5%E5%BD%B1-imdb%E5%92%8C%E7%83%82%E7%95%AA%E8%8C%84%E8%AF%84%E5%88%86%E6%98%BE%E7%A4%BA) 安装本插件

## 使用说明

### 配置 IMDb 评分（必须）

IMDb 评分数据通过 **OMDb API** 获取，需要一个免费的 API Key 才能显示。

> **为什么需要 API Key？**
> 早期版本直接解析 IMDb 网页，但 IMDb 目前部署了 Cloudflare 防护，脚本发出的请求几乎必然被拦截，导致评分无法加载。切换到 OMDb API 后，数据获取稳定可靠。OMDb 免费计划每天有 1000 次额度，日常使用完全足够。

**获取步骤（约 2 分钟）：**

1. 打开 [omdbapi.com/apikey.aspx](https://www.omdbapi.com/apikey.aspx)
2. 选择 **FREE**（免费，每天 1000 次，个人使用完全够用）
3. 填写邮箱，点击 Submit
4. 去邮箱收一封来自 OMDb 的激活邮件，点击邮件中的激活链接
5. 激活成功后，邮件中即有你的 API Key（格式类似 `a1b2c3d4`）

**填入 API Key：**

1. 在任意豆瓣电影页面，点击浏览器工具栏的 **Tampermonkey 图标**
2. 在弹出菜单中找到"**设置 OMDb API Key**"并点击
3. 在输入框中粘贴你的 API Key，点击确定
4. 刷新页面，IMDb 评分即可显示

![设置 OMDb API Key](https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/screenshots/set-omdb-api-key.png)

> 不配置 API Key 也可以正常使用，但 IMDb 评分区域会显示"未配置"，烂番茄评分不受影响。

### 首次使用权限授权

首次访问豆瓣电影页面时，Tampermonkey 会弹出权限请求，建议点击"**总是允许**"。

### 使用须知
- 需要能访问 [www.rottentomatoes.com](https://www.rottentomatoes.com) 和 [www.omdbapi.com](https://www.omdbapi.com)（需要科学上网）
- 豆瓣页面无 IMDb 词条的电影无法显示任何评分
- 烂番茄评分可能因电影名称匹配不准确而显示错误

### 关于评分
- 烂番茄图标含义：[About Rotten Tomatoes®](https://www.rottentomatoes.com/about)
- IMDb评分常见问题：[IMDb Ratings FAQ](https://help.imdb.com/article/imdb/track-movies-tv/ratings-faq/G67Y87TFYYP6TWAV?showReportContentLink=false#)

## 兼容性
- Edge 最新版
- Chrome 最新版
- Firefox 最新版
- Safari 最新版

## License
[MIT License](LICENSE)

## TODO

### 功能
- [ ] 添加烂番茄评分人数显示
- [ ] 优化烂番茄电影名称匹配算法
- [ ] 添加功能模块的设置开关
- [ ]  *添加MetaCritic评分支持(待定)*

### 错误
- [ ] 某些电影页面的爆米花图标显示问题


## 项目地址
<a href="https://github.com/f-is-h/douban-imdb-rt" target="_blank">
    <img src="https://raw.githubusercontent.com/f-is-h/douban-imdb-rt/main/assets/icon/github.png" width="99" height="99"/>
</a>