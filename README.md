## Usage

- 一、注册 GitHub
  
- 二、Fork [this GitHub repository](https://github.com/sypopo/Actions-OpenWrt)
  
- 三、生成`.config`文件方法：  
  
首先`git clone https://github.com/coolsnowwolf/lede`  
  
然后添加 `src-git lienol https://github.com/Lienol/openwrt-package` 到 feeds.conf.default 文件 并执行以下命令： 
```bash
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
```
最后输入 `make menuconfig` 命令选插件，选好插件后执行 `./scripts/diffconfig.sh > seed.config` 根目录中会生成一个`seed.config`文件。
  
- 四、触发 Actions 进行编译 
  
在自己fork出来的项目里的网页里创建一个新文件(点击Create new file) ， 然后把前面提到的`seed.config`文件的内容粘贴进来，文件名写`.config`然后直接点提交。就会触发自动编译，点击Actions就能看到编译的状况。
  
- 五、下载固件  
  
要下载固件的话，等他编译完（一般需要2小时），进项目的Actions页面，点页面左侧的Build OpenWrt查看编译详情，页面`Artifacts`有个`OpenWrt firmware`就是你要的固件，点击下载。
  
## Screenshot
![image](https://github.com/sypopo/Actions-OpenWrt/blob/master/20191225135809.png)
![image](https://github.com/sypopo/Actions-OpenWrt/blob/master/20191225135919.png)

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
