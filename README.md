## Usage

- Sign up for [GitHub Actions](https://github.com/features/actions/signup)
- Fork [this GitHub repository](https://github.com/sypopo/Actions-OpenWrt)
- Generate `.config` files using [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) source code.并按此操作执行：  
添加 src-git lienol https://github.com/Lienol/openwrt-package 到 feeds.conf.default 文件  
./scripts/feeds clean  
./scripts/feeds update -a  
rm -rf feeds/lienol/package/v2ray  
rm -rf feeds/lienol/package/openssl1.1  
rm -rf feeds/lienol/package/trojan  
rm -rf feeds/lienol/package/ipt2socks  
rm -rf feeds/lienol/package/shadowsocksr-libev  
rm -rf feeds/lienol/package/pdnsd-alt  
rm -rf package/lean/kcptun  
rm -rf package/lean/verysync  
rm -rf package/lean/luci-app-kodexplorer  
rm -rf package/lean/luci-app-pppoe-relay  
rm -rf package/lean/luci-app-pptp-server  
rm -rf package/lean/luci-app-v2ray-server  
rm -rf package/lean/luci-app-verysync  
./scripts/feeds install -a  
然后 make menuconfig 选插件，选好后执行 ./scripts/diffconfig.sh > seed.config 复制一下这个seed.config的文本内容到项目根目录的.config文件中。  

## Acknowledgments

- [Microsoft](https://www.microsoft.com)
- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub](https://github.com)
- [GitHub Actions](https://github.com/features/actions)
- [tmate](https://github.com/tmate-io/tmate)
- [mxschmitt/action-tmate](https://github.com/mxschmitt/action-tmate)
- [csexton/debugger-action](https://github.com/csexton/debugger-action)
- [Cisco](https://www.cisco.com/)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [Lienol's Openwrt-package](https://github.com/Lienol/openwrt-package)
