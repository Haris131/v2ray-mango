# v2ray-mango

wget -O kuoruan-public.key http://openwrt.kuoruan.net/packages/public.key
opkg-key add kuoruan-public.key
wget -O kuoruan-public.key http://openwrt.kuoruan.net/packages/public.key
opkg-key add kuoruan-public.key
echo "src/gz kuoruan_packages http://openwrt.kuoruan.net/packages/releases/$(. /etc/openwrt_release ; echo $DISTRIB_ARCH)" \ >> /etc/opkg/customfeeds.conf
echo "src/gz kuoruan_universal http://openwrt.kuoruan.net/packages/releases/all" \ >> /etc/opkg/customfeeds.conf
opkg update
 
##kalo mau install v2ray core
opkg install v2ray-core
 
##kalo mau install v2ray core mini
opkg install v2ray-core-mini
 
##kalo mau install v2ray-core, jangan install v2ray-core-mini, begitu juga sebaliknya.
 
##install luci app v2ray
opkg install luci-app-v2ray
 
##kalo error "But that file is already provided by package * dnsmasq"
opkg remove dnsmasq
opkg install luci-app-v2ray
 
