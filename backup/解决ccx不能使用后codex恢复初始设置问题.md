我看到网上介绍ccx加codex可以使用，结果使用一会就出问题了，现在我想恢复codex初始设置怎么做？

<img width="1122" height="508" alt="Image" src="https://github.com/user-attachments/assets/05899e49-ea9a-4efe-9365-40e03859a75c" />

## Codex 恢复初始设置 + 解决127.0.0.1:3688断开报错分步方案：
报错stream disconnected before completion: http://127.0.0.1:3688/v1/responses
是CCX 转发代理配置残留，CCX 修改了 Codex 的 API 地址指向本地 3688 端口，
代理进程挂掉就持续重连报错，按下面步骤彻底重置回官方初始配置（你是 Mac 系统）。

一、先完全关闭 Codex 客户端 + CCX 程序
1退出 Codex 桌面软件（右上角完全退出）
2终端执行，杀掉残留端口进程：

```
# 杀掉3688端口CCX代理
lsof -i :3688 | awk '{print $2}' | xargs kill -9
```
## 解决方案 ：
一键彻底全量恢复出厂初始设置（配置全清空，等于全新安装）
```
# 备份原有配置（可选，需要还原时恢复）
cp -r ~/.codex ~/.codex_ccx_bak
# 删除全部配置目录，Codex下次启动自动生成全新默认配置
rm -rf ~/.codex
```