# 地图选点与收藏

个人地图面板。支持地图图层切换、经纬度搜索、保存当前选点和管理收藏。

## Cloudflare Pages

- 框架预设选择 `None`，构建命令留空或填 `exit 0`，输出目录填 `public`。
- 生产环境添加加密变量 `TOKEN`，并添加 KV 绑定 `SPOOFER_DATA`。
- 可选变量 `AMAP_KEY` 用于浏览器端高德地点搜索。若使用，请按高德支持的方式限制密钥用途。
- 设置变量或绑定之后重新部署。访问 Pages 站点，在登录框输入 `TOKEN` 的值。

地图瓦片、地点搜索和海拔查询会向所选地图服务发送相关请求。保存坐标和收藏通过同源 Pages Functions 写入 KV。

基于 [akudamatata 的原始项目](https://github.com/akudamatata/iOS-Location-Spoofer-Web) 修改。
原项目内容使用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 授权。Leaflet 组件的许可证见 `public/leaflet/LICENSE`。
