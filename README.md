# Cloudflare-ddns
使用 Cloudflare API，支持 IPv4，轻松地更新 DNS，还可添加定时任务达到自动更新 IP 的目的。

一、下载脚本：

wget -qO /usr/local/bin/cf-ddns.sh https://raw.githubusercontent.com/cnyangang/Cloudflare-ddns/master/cfddns.sh

二、使用方法：

1、修改脚本中 CFKEY，CFUSER，CFZONE_NAME，CFRECORD_NAME 对应内容为自己的信息

2、给脚本执行权限 chmod +x /usr/local/bin/cf-ddns.sh

3、执行 crontab -e 并添加以下定时任务：*/1 * * * * /usr/local/bin/cfddns.sh  #每分钟执行一次

怎么获取我的 Cloudflare API？ 

访问 https://www.cloudflare.com/a/account/my-account ，在上方选择 API Tokens 标签页，然后查看页面下方的 Global API Key。
