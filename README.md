# skynet_ssl
由于项目去接第三方sdk，需要用到https链接，而我用skynet服务器框架本身没有提供，需要自己加上一个。openssl编程中文资料很少，网上我找到一个，可是他在做tsl的时候，tcp链接是自己创建socket，而skynet已经做了这部分事情，我不想破坏原有的设计，我需要自己只是单独添加协议，tcp读写都由现有的skynet提供。此库只提供了为lua封装的c代码，lua代码我是直接拿skynet http库的sockhelper改的，原来直接调用skynet socket读写，先改成直接调用此库的读写接口，并让此库去直接控制skynet socket读写。
