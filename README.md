对接企业微信应答：
https://github.com/lanrion/qy_wechat

(对应公众号gem：https://github.com/lanrion/weixin_rails_middleware)

由于工作太忙，目前wiki没有完善，这里简要说明：

## 安装

通过：
```ruby
gem 'qy_wechat', git: 'https://github.com/lanrion/qy_wechat.git'
# or
gem 'qy_wechat', '~> 1.0.0.beta1'
```
安装。

## 使用

基本上保持 https://github.com/lanrion/weixin_rails_middleware 的使用一致。

```ruby
rails g qy_wechat:install
rails g qy_wechat:migration QyAccount # QyAccount 你保存企业号的Model
```
分别会产生:

配置保存你企业信息的Model: `qy_wechat_example/config/initializers/qy_wechat_config.rb`

这里实现你的业务逻辑:  `qy_wechat_example/app/decorators/controllers/qy_wechat/qy_wechat_controller_decorator.rb`

## 生成服务验证URL

`qy_wechat_engine.qy_verify_url(qy_account.qy_secret_key)`
