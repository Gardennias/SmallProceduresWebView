# miniprogramWebView
小程序与网页通讯

## 运行环境
Hbuilder


## 项目结构 
目录生成工具 [mddir](https://www.npmjs.com/package/mddir)
```
|-- miniprogramWebView
    |-- App.vue
    |-- main.js
    |-- manifest.json
    |-- pages.json
    |-- README.md
    |-- uni.scss
    |-- pages
    |   |-- component  
    |   |   |-- button
    |   |       |-- button.vue    // 从web 跳转到 小程序页面
    |   |-- index
    |   |   |-- index.vue        // 小程序 首页
    |   |-- web-view
    |       |-- web-view.vue    // web-view
    |-- static
        |-- logo.png
        |-- test.html          // web-view 引入的 web 源码，只做参考，不可直接再本项目直接引用，可单独部署到服务器
```

### test.html

在编写访问外部的html时，除了需要加入 [微信小程序 JS-SDK](https://res.wx.qq.com/open/js/jweixin-1.4.0.js)
> <script type="text/javascript" src="https://res.wx.qq.com/open/js/jweixin-1.4.0.js"></script>
同时还需要加入 [uni 的 SDK](https://js.cdn.aliyun.dcloud.net.cn/dev/uni-app/uni.webview.1.5.1.js)
> <script type="text/javascript" src="https://js.cdn.aliyun.dcloud.net.cn/dev/uni-app/uni.webview.1.5.1.js"></script>

经测试，uni SDK 只能使用 uni 路由与页面跳转命令：即 该项目中的 web页展示
> uni.navigateTo  uni.redirectTo  uni.reLaunch  uni.switchTab

具体可参考 [uni-app官方示例html](https://uniapp.dcloud.io/static/web-view.html)
右击查看网页源代码
