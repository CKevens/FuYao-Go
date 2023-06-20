# FuYao - Go 扶摇直上九万里 - 不再开源 维护中...

- [**个人博客**](https://blog.yunjianxx.com/) **- 专注分享信息安全新技术、新领域的技术和知识的学习笔记，不时发布原创实用安全工具、安全脚本.**
- [**在线武器库**](https://link.yunjianxx.com/) **- 提供安全、渗透、社工等方面书签｜为广大网络安全爱好者提供网站导航,为小白提供黑客入门网站的安全站点收集.**
- 😄 I’m ExpLang [**Twitter**](https://twitter.com/ExpLang_Cn)

## [问题反馈](https://github.com/ExpLangcn/FuYao-Go/issues)|[漏洞列表](https://github.com/ExpLangcn/FuYao-Go/blob/main/README.md#%E6%BC%8F%E6%B4%9E%E5%88%97%E8%A1%A8)

**自动化进行目标资产探测和安全漏洞扫描｜适用于赏金活动、SRC活动、大规模使用、大范围使用|通过使用被动在线资源来发现网站的有效子域｜使用零误报的定制模板向目标发送请求，同时可以对大量主机进行快速扫描。｜提供TCP、DNS、HTTP、FILE等各类协议的扫描，通过强大且灵活的模板，模拟各种安全检查**

<img width="899" alt="image" src="https://user-images.githubusercontent.com/52586866/168596909-c0f95cff-1460-4af7-8d4a-7e5afde3f30e.png">

<img width="1738" alt="image" src="https://user-images.githubusercontent.com/52586866/168596925-b2a50a21-df0a-433d-8424-cd2d5386b5be.png">

## 法律免责声明
本工具仅面向合法授权的企业安全建设行为，如您需要测试本工具的可用性，请自行搭建靶机环境。 在使用本工具进行检测时，您应确保该行为符合当地的法律法规，并且已经取得了足够的授权。请勿对非授权目标进行扫描。 如果发现上述禁止行为，我们将保留追究您法律责任的权利。

如您在使用本工具的过程中存在任何非法行为，您需自行承担相应后果，我们将不承担任何法律及连带责任. 您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。

----

### 更新记录
**2022.6.6 14.59**
 - 新增Hunter网络测绘扫描
 - 新增 `-p` 参数 可以指定漏洞文件夹（采用xray漏洞模版,如果直接拿过来，语言name改为id ,Details改为 info,不支持cache ）

**2022.5.16 20:45**
 - 发布V1.3.2版本
 - 修复个别情况无法进行Shodan扫描
 - 新增Quake资产获取
 - 优化存活验证逻辑
 - 新增端口探测（探测完子域名后会进行存活探测，存活探测的同时会进行端口探测）
 - 优化输出信息
 - 新增新版本检查（在启动LOGO上可以看到最新版本）

**2022.5.11 12:10**
 - 发布V1.3版本
 - 子域名探测效率提升
 - 新增自动FoFa资产探测
 - 新增自动Shodan资产探测
 - 更换漏洞库和验证库 - [Afrog](https://github.com/ExpLangcn/FuYao-Go)
 - 新增指纹探测识别

**2022.4.15 17:10**
 - 发布V1.1版本
 - 修复Windows下 file missing [file=MANIFEST-000000] 错误
 - 修复Windows下 no valid templates were found 报错
 - 优化扫描并发配置

**2022.4.15 12:00**
 - 发布 v1.0版本

----

### 当前功能 or 未来功能

- [x] 子域名枚举资产收集
- [x] 批量子域名枚举资产收集
- [x] Chaos 资产收集
- [x] 资产存活验证
- [x] 批量资产存活验证
- [x] 安全漏洞验证
- [x] 批量安全漏洞验证
- [x] 子域名枚举资产收集、资产存活验证、安全漏洞扫描联动
- [x] FoFa自动资产探测
- [x] Shodan自动资产探测
- [x] Web指纹探测识别
- [x] 网络空间测绘资产收集
- [x] 中间件漏洞利用例：shiro、SpringBoot等...
- [x] Hunter自动资产探测
- [ ] 子域名存活WebHook通知
- [ ] 安全漏洞扫描结果WebHook通知
- [ ] 待定...

**有需要什么功能的话可以在 [issues](https://github.com/ExpLangcn/FuYao-Go/issues) 提**

----

### 当前POC列表

#### [点击查看详情](https://github.com/ExpLangcn/FuYao-Go/blob/main/README.md#%E6%BC%8F%E6%B4%9E%E5%88%97%E8%A1%A8)

当前总共有：**549个POC模版**

<img width="254" alt="image" src="https://user-images.githubusercontent.com/52586866/167674307-3a3e39f9-3a76-4132-ba23-7bff624307e3.png">

----

### 使用帮助

#### 不推荐使用Windows系统！

```
./mark/FuYao_Intel/FuYao_Intel -h                                                                                                                                                                          FuYao_test
  ███████╗██╗   ██╗██╗   ██╗ █████╗  ██████╗
  ██╔════╝██║   ██║╚██╗ ██╔╝██╔══██╗██╔═══██╗
  █████╗  ██║   ██║ ╚████╔╝ ███████║██║   ██║
  ██╔══╝  ██║   ██║  ╚██╔╝  ██╔══██║██║   ██║  Version: V1.3
  ██║     ╚██████╔╝   ██║   ██║  ██║╚██████╔╝  Author: ExpLang
  ╚═╝      ╚═════╝    ╚═╝   ╚═╝  ╚═╝ ╚═════╝   Discord: ExpLang#6666
     Github:github.com/ExpLangcn/FuYao-Go
 使用FuYao前请遵守当地法律,FuYao仅提供给教育行为使用

 法律免责声明
  本工具仅面向合法授权的企业安全建设行为，如您需要测试本工具的可用性，请自行搭建靶机环境。
  在使用本工具进行检测时，您应确保该行为符合当地的法律法规，并且已经取得了足够的授权。请勿对非授权目标进行扫描。
  如果发现上述禁止行为，我们将保留追究您法律责任的权利。

  如您在使用本工具的过程中存在任何非法行为，您需自行承担相应后果，我们将不承担任何法律及连带责任.
  您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。

Usage of ./mark/FuYao_Intel/FuYao_Intel:
  -f string
        指定根域目标文件 ｜ 支持绝对路径和相对路径
```

**自动化信息搜集+漏洞扫描**(目标文件内的目标是一行一个，并且必须是主域名)

> ./FuYao -f list.txt

----

### 配置信息

```
FoFa:
  email: ""
  key: ""
Shodan:
  key: ""
```
----

### 联系方式

#### WeChat

<img src="https://tva1.sinaimg.cn/large/e6c9d24egy1h17yaq5zf6j20u012aq5x.jpg" alt="image-20220413113316684" style="zoom: 33%;" />

#### **[加入Discord](https://discord.gg/GCZzJmzW3G)**

----

### 漏洞列表

|  漏洞列表   |
| ---- |
|d-link-router-command-injectio|
|stop_if_match_tes|
|CVE-2013-225|
|CVE-2014-627|
|CVE-2014-312|
|CVE-2014-370|
|CVE-2022-2313|
|CVE-2022-2556|
|CVE-2022-2508|
|CVE-2022-2499|
|CVE-2022-2137|
|CVE-2022-2412|
|CVE-2022-2426|
|CVE-2022-2294|
|CVE-2022-2946|
|CVE-2022-2536|
|CVE-2022-2411|
|CVE-2022-2317|
|CVE-2022-2313|
|CVE-2022-054|
|CVE-2022-2295|
|CVE-2015-839|
|CVE-2015-333|
|CVE-2015-142|
|CVE-2015-729|
|CVE-2015-553|
|CVE-2012-182|
|CVE-2017-552|
|CVE-2017-1027|
|CVE-2017-1214|
|CVE-2017-792|
|CVE-2017-1161|
|CVE-2017-979|
|CVE-2017-984|
|CVE-2017-1261|
|CVE-2017-1687|
|CVE-2017-1263|
|CVE-2017-100002|
|CVE-2017-1262|
|CVE-2017-891|
|CVE-2017-750|
|CVE-2010-187|
|CVE-2010-286|
|CVE-2019-1675|
|CVE-2019-1631|
|CVE-2019-1699|
|CVE-2019-844|
|CVE-2019-1151|
|CVE-2019-019|
|CVE-2019-1699|
|CVE-2019-1839|
|CVE-2019-1998|
|CVE-2019-1755|
|CVE-2019-2008|
|CVE-2019-844|
|CVE-2019-379|
|CVE-2019-719|
|CVE-2019-1158|
|CVE-2019-1750|
|CVE-2019-1666|
|CVE-2019-1075|
|CVE-2019-1978|
|CVE-2019-1741|
|CVE-2019-1272|
|CVE-2019-723|
|CVE-2019-2022|
|CVE-2019-1510|
|CVE-2019-272|
|CVE-2019-845|
|CVE-2019-512|
|CVE-2019-1627|
|CVE-2019-272|
|CVE-2019-967|
|CVE-2019-634|
|CVE-2019-1609|
|CVE-2019-339|
|CVE-2019-1692|
|CVE-2021-2197|
|CVE-2021-4134|
|CVE-2021-365|
|CVE-2021-4177|
|CVE-2021-322|
|CVE-2021-2197|
|CVE-2021-2685|
|CNVD-2021-4237|
|CVE-2021-2298|
|CVE-2021-2816|
|CVE-2021-301|
|CVE-2021-2123|
|CVE-2021-2608|
|CVE-2021-4043|
|CVE-2021-2790|
|CVE-2021-2528|
|CVE-2021-3180|
|CVE-2021-312|
|CVE-2021-3304|
|CVE-2021-2220|
|CVE-2021-2608|
|CVE-2021-3674|
|CVE-2021-2221|
|CVE-2021-2962|
|CVE-2021-2140|
|CVE-2021-4445|
|CVE-2021-3626|
|CVE-2021-4328|
|CVE-2021-3758|
|CVE-2021-2198|
|CVE-2021-3160|
|CVE-2020-2798|
|CVE-2020-2818|
|CVE-2020-528|
|CVE-2020-345|
|CVE-2020-937|
|CVE-2020-820|
|CVE-2020-2818|
|CVE-2020-798|
|CVE-2020-1475|
|CVE-2020-949|
|CVE-2020-541|
|CVE-2020-590|
|CVE-2020-3547|
|CVE-2020-975|
|CVE-2020-819|
|CVE-2020-1014|
|CVE-2020-551|
|CVE-2020-2122|
|CVE-2020-2457|
|CVE-2020-819|
|CVE-2020-2641|
|CVE-2020-851|
|CVE-2020-540|
|CVE-2020-1751|
|CVE-2020-948|
|CVE-2020-1393|
|CVE-2020-1417|
|CVE-2020-1145|
|CVE-2020-3573|
|CVE-2020-1684|
|CVE-2020-1418|
|CVE-2020-1020|
|CVE-2020-1171|
|CVE-2020-2818|
|CVE-2020-1556|
|CVE-2020-1019|
|CVE-2020-2507|
|CVE-2018-803|
|CVE-2018-877|
|CVE-2018-1073|
|CVE-2018-1337|
|CVE-2018-376|
|CVE-2018-1073|
|CVE-2018-1175|
|CVE-2018-999|
|CVE-2018-760|
|CVE-2018-731|
|CVE-2018-100053|
|CVE-2018-1261|
|CVE-2018-691|
|CVE-2018-100060|
|CVE-2018-766|
|CVE-2018-100086|
|CVE-2018-770|
|CVE-2018-1073|
|CVE-2018-660|
|CVE-2018-1724|
|CVE-2018-1168|
|CVE-2018-1912|
|CVE-2018-1073|
|CVE-2018-749|
|CVE-2016-308|
|CVE-2016-497|
|CVE-2016-1013|
|CVE-2016-308|
|directadmin-login-pane|
|microsoft-exchange-pane|
|terramaster-pane|
|swagger-api-disclosur|
|kubernetes-versio|
|thinkphp-detec|
|rocketmq-console-exposu|
|django-admin-pane|
|adminer-pane|
|zentao-detec|
|kubernetes-metric|
|phpmyadmin-pane|
|azure-kubernetes-servic|
|apisix-pane|
|dlink-pane|
|mongodb-ops-manage|
|sonicwall-sslvpn-pane|
|jenkins-logi|
|utt-pane|
|jenkins-api-pane|
|landrayoa-pane|
|weblogic-pane|
|openerp-databas|
|gitlab-pane|
|minio-consol|
|wayos-pane|
|emessage-pane|
|solarwinds-orion-pane|
|tomcat-detec|
|avtech-avn801-camera-pane|
|huawei-hg532e-pane|
|kubernetes-miranti|
|jupyter-notebook-tec|
|grafana-detec|
|activemq-pane|
|wordpress-logi|
|fckedito|
|upupw-pane|
|kubernetes-dashboar|
|sonicwall-management-pane|
|minio-browse|
|kubernetes-resource-repor|
|rabbitmq-dashboar|
|shiro-detec|
|zabbix-pane|
|kubernetes-enterprise-manage|
|jira-pane|
|dubbo-detec|
|CNVD-200705-31|
|CNVD-2017-2007|
|CNVD-2019-0134|
|CNVD-2019-3413|
|CNVD-2019-2223|
|CNVD-2019-1679|
|CNVD-2021-0412|
|CNVD-2021-1582|
|CNVD-2021-1054|
|CNVD-2021-3901|
|CNVD-2021-1453|
|CNVD-2021-0965|
|CNVD-2021-1582|
|CNVD-2020-5882|
|CNVD-2020-6711|
|CNVD-2020-5726|
|CNVD-2020-2373|
|CNVD-2020-6242|
|CNVD-2018-1339|
|kyan-network-monitoring-account-password-leakag|
|ruijie-smartweb-password-disclosur|
|avtech-password-disclosur|
|alibaba-canal-info-lea|
|seeyon-oa-cookie-lea|
|huawei-dg8045-home-gateway-exposure|
|hjtcloud-directory-file-lea|
|laravel-debug-info-lea|
|seeyon-a6-employee-info-lea|
|phpinfo-disclosur|
|tianqing-info-lea|
|go-pprof-lea|
|aspcms-backend-lea|
|nsfocus-uts-password-lea|
|thinkphp-509-information-disclosur|
|avtech-dvr-exposur|
|dlink-850l-info-lea|
|ruijie-eg-info-lea|
|seeyon-session-lea|
|tongda-user-session-disclosur|
|ruijie-nbr1300g-cli-password-lea|
|hadoop-disclosur|
|openvpn-monitor-disclosur|
|hikvision-info-lea|
|e-office-mysql-config-lea|
|mobileiron-log4j-jndi-rc|
|springboot-log4j-rc|
|apache-ofbiz-log4j-rc|
|CV|
|resin-inputfile-filerea|
|natshell-arbitrary-file-rea|
|thinkadmin-v6-readfil|
|sangfor-ba-rc|
|ruoyi-management-filerea|
|e-cology-springframework-directory-traversa|
|thinkphp-501-rc|
|flink-upload-rc|
|huijietong-cloud-filerea|
|jumpserver-unauth-rc|
|thinkphp-v6-file-writ|
|WOOYUN-2010-08072|
|thinkphp-2-rc|
|odoo-file-rea|
|amtt-hiboss-server-ping-rc|
|unifi-network-log4j-rc|
|kingdee-eas-directory-traversa|
|maccms-rc|
|e-cology-v8-sql|
|powercreator-arbitrary-file-uploa|
|shiziyu-cms-apicontroller-sql|
|vmware-vcenter-arbitrary-file-rea|
|seeyon-session-upload-webshel|
|solr-file-rea|
|duomicms-sql|
|cacti-weathermap-file-writ|
|ruijie-eg-file-rea|
|weiphp-path-traversa|
|zzcms-zsmanage-sql|
|showdoc-uploadfil|
|phpok-sql|
|landray-oa-custom-jsp-filerea|
|dockercfg-confi|
|seeyon-wooyun-2015-14822|
|hjtcloud-arbitrary-filerea|
|qilin-bastion-host-rc|
|springboot-h2-db-rc|
|samsung-wea453e-rc|
|finereport-directory-traversa|
|docker-registr|
|yapi-rc|
|tamronos-iptv-rc|
|fangweicms-sql|
|vrealize-operations-log4j-rc|
|nuuo-file-inclusio|
|egroupware-rc|
|yongyou-u8-oa-sql|
|phpshe-sql|
|sangfor-edr-cssp-rc|
|seacms-sql|
|sangfor-edr-arbitrary-admin-logi|
|couchdb-adminpart|
|yonyou-nc-arbitrary-file-uploa|
|yonyou-nc-bsh-servlet-bshservlet-rc|
|discuz-v72-sql|
|feifeicms-lf|
|landray-oa-syssearchmain-rc|
|samsung-wea453e-default-pw|
|laravel-improper-webdi|
|e-cology-javabeanshell-rc|
|mpsec-isg1000-file-rea|
|tpshop-sql|
|e-cology-syncuserinfo-sql|
|thinkcmf-lf|
|ecshop-collection-list-sql|
|dahua-dss-file-rea|
|etouch-v2-sql|
|sangfor-edr-tool-rc|
|dlink-dsl-2888a-rc|
|hanming-video-conferencing-file-rea|
|msvod-sql|
|wanhuoa-fileupload-controller-uploa|
|thinkphp-5023-rc|
|thinkphp-5022-rc|
|yonyou-grp-u8-sqli-to-rc|
|grafana-file-rea|
|discuz-wechat-plugins-unaut|
|samsung-wlan-ap-wea453e-rc|
|seacms-rc|
|huawei-home-gateway-hg659-filerea|
|docker-remote-ap|
|xdcms-sq|
|seeyon-wooyun-2015-0108235-sql|
|sonicwall-ssl-vpn-rc|
|solr-admin-quer|
|dedecms-membergroup-sql|
|jeewms-showordownbyurl-filerea|
|ns-asg-file-rea|
|wuzhicms-v410-sql|
|seacms-before-v992-rc|
|wordpress-ext-mailpress-rc|
|e-cology-arbitrary-file-uploa|
|e-cology-validate-sql|
|solr-log4j-rc|
|spon-ip-intercom-ping-rc|
|yungoucms-sql|
|dotnetcms-sql|
|yccms-rc|
|typecho-rc|
|joomla-component-vreview-sq|
|wordpress-ext-adaptive-images-lf|
|resin-viewfile-filerea|
|pbootcms-database-file-downloa|
|tpshop-directory-traversa|
|weiphp-sq|
|metinfo-file-rea|
|consul-service-rc|
|phpstudy-backdoor-rc|
|thinkcmf-write-shel|
|zcms-v3-sql|
|dedecms-url-redirectio|
|weblogic-ssr|
|seacms-v654-rc|
|consul-rexec-rc|
|seacmsv645-command-exe|
|spring-cloud-function-spel-rc|
|targa-camera-lf|
|netentsec-ngfw-rc|
|phpstudy-nginx-wrong-resolv|
|h3c-secparh-any-user-logi|
|dedecms-carbuyaction-fileinclud|
|h3c-imc-rc|
|myucms-lf|
|dedecms-guestbook-sql|
|spon-ip-intercom-file-rea|
|finecms-sql|
|e-cology-workflowcentertreedata-sql|
|e-bridge-saveyzjfile-file-rea|
|iis-put-getshel|
|e-cology-getsqldata-sql-injec|
|anyproxy-directory-traversa|
|kingsoft-v8-file-rea|
|yonyou-grp-u8-sql|
|maccmsv10-backdoo|
|phpmyadmin-setup-deserializatio|
|ecshop-rc|
|qibocms-sql|
|e-cology-filedownload-directory-traversa|
|ruijie-eg-cli-rc|
|jira-unauthenticated-user-picke|
|frp-dashboard-unaut|
|jira-unauthenticated-resolution|
|jira-unauthenticated-project|
|pyspider-unauthorized-acces|
|elasticsearch-unaut|
|jeecg-boo|
|jira-unauthenticated-adminproject|
|hadoop-yarn-unaut|
|hp-officepro-printer-unauthorize|
|zabbix-dashboards-acces|
|jboss-unaut|
|druid-monitor-unaut|
|kubernetes-unaut|
|seeyon-ajax-unauthorized-acces|
|springboot-actuator-unaut|
|zabbix-authentication-bypas|
|airflow-unaut|
|nacos-v1-auth-bypas|
|kibana-unaut|
|influxdb-unaut|
|tongda-meeting-unauthorized-acces|
|couchdb-unauthorize|
|jira-unauthenticated-installed-gadget|
|jupyter-notebook-unauthorized-acces|
|kafka-manager-unaut|
|jira-service-desk-signu|
|storm-unauthorized-acces|
|spark-api-unaut|
|jira-unauthenticated-screen|
|qizhi-fortressaircraft-unauthorize|
|spark-webui-unaut|
|jira-unauthenticated-dashboard|
|ruoyi-cms-unaut|
|jira-unauthenticated-projectcategorie|
|tensorboard-unaut|
|bt742-pma-unauthorized-acces|
|etcd-unaut|
|jenkins-unauthorized-acces|
|h2-database-web-console-unauthorized-acces|
|nifi-api-unauthorized-acces|
|spectracom-default-passwor|
|chinaunicom-default-logi|
|rseenet-default-passwor|
|weblogic-weak-logi|
|rancher-default-passwor|
|showdoc-default-passwor|
|dlink-default-passwor|
|wayos-default-passwor|
|kingsoft-v8-default-passwor|
|ambari-default-passwor|
|zabbix-default-passwor|
|rabbitmq-default-passwor|
|trilithic-viewpoint-default-passwor|
|nexus-default-passwor|
|activemq-default-passwor|
|gitlab-weak-logi|
|ofbiz-default-passwor|
|jinher-oa-c6-default-passwor|
|ibm-storage-default-passwor|
|oracle-business-intelligence-passwor|
|netentsec-icg-default-passwor|
|seeddms-default-passwor|
|ricoh-weak-passwor|
|kafka-center-default-passwor|
|tomcat-default-logi|
|nsicg-default-passwor|
|azkaban-default-passwor|
|jenkins-default-pw|
|mofi4500-default-passwor|
|minio-default-passwor|
|utt-default-passwor|
|axis2-default-passwor|
|hikvision-intercom-service-default-passwor|
|dell-idrac9-default-passwor|
|alibaba-canal-default-passwor|
|versa-default-passwor|
|exacqvision-default-passwor|
|panabit-ixcache-default-passwor|
|openerp-default-passwor|
|grafana-default-passwor|
|datang-ac-default-password-cnvd-2021-0412|
|dubbo-admin-default-passwor|
|jmx-default-passwor|
|nps-default-passwor|
|telecom-gateway-default-passwor|
|aolynk-br304-default-passwor|
|rockmongo-default-passwor|
|xerox7-default-passwor|
|secnet-ac-default-passwor|
|panabit-gateway-default-passwor|
|arl-default-passwor|
|CVE-2015-745|
|phpmyadmin-setu|
|CVE-2021-4422|
|CVE-2020-1392|
|alphaweb-default-passwor|
|pma-server-impor|
|phpmyadmin-misconfiguration

### Stargazers over time

[![Stargazers over time](https://starchart.cc/ExpLangcn/FuYao-Go.svg)](https://starchart.cc/ExpLangcn/FuYao-Go)
