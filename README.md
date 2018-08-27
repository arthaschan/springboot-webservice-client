解决办法:
    出现这个问题的第一时间，我以为是常规的maven管理jar包依赖问题。后面群里有小伙伴多次尝试证明了不是maven的依赖包问题。而是spring boot的版本和cxf的版本不兼容问题。
已知兼容版本:
Spring boot 1.4.x ------>cxf-spring-boot-starter-jaxws 3.1.x
Spring boot 1.5.x------->cxf-spring-boot-starter-jaxws 3.2.x
所以出现上面问题,且用了spring boot 1.5.x的小伙伴请将cxf-spring-boot-starter-jaxws 版本升级到3.2.1即可解决。

3.2修改spring boot cxf整合后默认的/services路径
在spring boto的application配置文件中配置
cxf.path=/yourpath