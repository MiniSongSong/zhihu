## 主线功能
* 注册 + 登录 + 设置 √
* 提问 + 回答 + 点赞 √
* 关注问题 + 动态推送 √
* 关注人 + （赞、提出问题、关注问题、回答问题）  正在做

## 问题
* 抓了知乎登录的包，发现是明文账号密码。。但是我这个demo就不用https了。
* RESTful,表单提交不支持put,delete,就用post代替，用ajax的时候满足RESTful风格。
* 目前响应式支持很糟糕。
* js/css都没有压缩，sass只用了简单的嵌套功能，js没有模块化
* 做完这个项目，学习一个gulp构建工具
* 想找个实习，想要团队合作，想要与牛人为伍。
* 聚合索引，排序~~~Topic那里要改。
* 修改回答，以及二级回答等到用了uEditor再加。先做推送。
* topic这个表没有必要。
* 明天做的：@和分享就不做了，二级评论、编辑回答先不做，先做关注问题，和推送回答。之后再做关注人，推送人的赞同。
* 做完后检查下索引齐了没。

## 功能-我喜欢的小细节
* 注册登录
    * 密码md5简单加盐加密
    * cookie签名，防篡改
    * 邮箱或手机号任意注册
    * 记住密码，可注销。
    * 权限中间件------------还要完善
* 设置：修改头像、姓名、邮箱或手机、密码
* 查询：只有非常简单的查询问题标题的功能
* 提问：模态层
* 评论
    * 点赞！上上、下下、上下、下上抵消，在问题中点过赞和down的再进入该页面会有赞和down的区别。
* 首页
    * 点击回答 会跳到该问题该回答处，页面被黄色覆盖渐变效果
* 问题页面
    * 相关问题
    * 日期（根据提交时间，格式：今天的显示【20:00】，昨天的显示【昨天20:00】，之前的显示【2015-08-31】）
* 404小彩蛋--最后加在app.js


## 没处理好、要改的细节 (√是基本解决的)
* url+'#id': 怎样才能距离顶部一些距离 ↓ 由于top栏固定占位50px，因此锚点被top栏覆盖
    * stackoverflow到 :target + padding-top 解决 √ 但是又有了新问题，会出现一段空白
    * 又stackoverfloooooooow,看到一个神解决，+ margin-top 负值。想了一下原理，会心一笑 √
* 注册、登录、提交问题都改成ajax
* 把权限登录改成中间件的形式 √
* 提问、回答没有换行 ----换编辑器
* 注册错误，重定向回来的时候，没有切换到注册Tab √
* index顶部navbar，用户下拉菜单的宽度 √   
* 记住密码，还没做！√


## 将要做的
* 登录页的推荐
* 富文本编辑器-先搁置，等基本功能都实现了再来完成这个
* 社交账号登录