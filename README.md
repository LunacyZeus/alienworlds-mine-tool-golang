# alienworlds-mine-tool-golang
alienworlds claim is low memory tool for alienworlds,it can monitor more than 100 account,and auto captcha and claim.

外星世界游戏辅助工具，基于golang开发的客户端，django开发的后台。通过后台自动调度账号达到同时挂几百个账号的目的。

感谢帮忙测试的小伙伴,目前已经挂了超过1000多个号了,就是需要很多服务器,正在优化,准备做个协议的版本的,这个其实就是eos币的流程  

目前实现功能  
1、支持本地算哈希 不需要开浏览器再算了（js速度不太行，之前用nodejs做了一个专门算hex的服务端，并发一高就宕机了，所以用golang重写了） 但是算完后claim需要开浏览器，目前用golang调用selenium做到了  
2、获取实时余额上传后台，这个用于批量账号管理的  
3、自动从后台获取需要挖矿的账号进行挖矿  
4、延迟 武器 地块缓存,降低挖矿时间 (因为没人会没事做去换武器和地块,这游戏难度是基于武器地块来计算的,每次把难度缓存到后台,下次挖矿的时候就不用去请求了,只需要请求少量网址,能提高挖矿速度)  
5、浏览器模式 可以提供会话token免登录直接到后台，这样方便后续提现操作  

待实现功能：  
1、自动claim nft道具。最近更新的这个功能，好像挖矿不掉武器了 需要单独创建tx请求，这个准备做个批量的工具（这个后面会开源）  
2、协议挖矿 大大提高挖矿速度,这里fd看了下 主要是要获取一个密钥然后push_transaction需要用,因为之前有谷歌验证码,我没办法协议过谷歌验证,现在好像去掉了,可以用请求做到~~~   

关于开源：  
1、不是我不开源，我也是想做开源项目的，结果被有心之人利用拿去倒卖，所以后面可以帮忙代挂或者我把关键功能丢服务器然后给工具跑~~ 真的怕了  
2、后面会把批量claim和后台管理开源了 可能没啥用~~~ 哈哈  

使用截图
![image](https://github.com/LunacyZeus/alienworlds-mine-tool-golang/raw/main/IMG_20210515_032104.jpg)
![image](https://github.com/LunacyZeus/alienworlds-mine-tool-golang/raw/main/QQ%E5%9B%BE%E7%89%8720210601190753.png)
![image](https://github.com/LunacyZeus/alienworlds-mine-tool-golang/raw/main/QQ%E6%88%AA%E5%9B%BE20210601190818.png)

联系邮箱：
68827626@qq.com
