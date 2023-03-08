Cloudflare API v4 Dynamic DNS Update in Bash, without unnecessary requests
Now the script also supports v6(AAAA DDNS Recoards)

修改脚本

# API key, see https://www.cloudflare.com/a/account/my-account,
# 上一步获取的CFKEY
CFKEY=
#输入你需要解析用来DDNS解析的根域名 eg: example.com
CFZONE=
# 暂时空着
CFID=
# 登陆CF的Username, eg: user@example.com
CFUSER=
# 填写用来DDNS解析的二级域名，与上面设置的要一致, eg: ddns.yourdomain.com
CFHOST=
# Cloudflare TTL for record, between 120 and 86400 seconds
CFTTL=3600
# Get domain ID from Cloudflare using awk/sed and python json.tool
GETID=true
# Ignore local file, update ip anyway
FORCE=false
# 填写上一步能正确返回咱的当前IP的网址, other examples are: bot.whatismyipaddress.com, https://api.ipify.org/ ...
WANIPSITE="myip.dnsomatic.com"
