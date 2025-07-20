# V2BX-SSPanel-UIM

<div align="center">

![V2BX Logo](https://img.shields.io/badge/V2BX-SSPanel--UIM-blue?style=for-the-badge)
![License](https://img.shields.io/github/license/q42602736/V2BX-SSPanel-UIM?style=for-the-badge)
![Release](https://img.shields.io/github/v/release/q42602736/V2BX-SSPanel-UIM?style=for-the-badge)
![Downloads](https://img.shields.io/github/downloads/q42602736/V2BX-SSPanel-UIM/total?style=for-the-badge)

**专为SSPanel-UIM面板优化的V2BX后端,注意本修改版V2BX后端只支持对接本人修改后的SSPanel-UIM项目，原项目可能不支持**
<br>[问题反馈](https://github.com/q42602736/V2BX-SSPanel-UIM/issues) · [📢 TG频道](https://t.me/fluentboard666)</br>

支持 VMess | VLESS+Reality | Shadowsocks2022 | Trojan | Hysteria2

</div>

---

## ✨ 特性

- 🚀 **完美对接SSPanel-UIM** - 原生支持SSPanel-UIM面板API
- 🔒 **多协议支持** - VMess、VLESS+Reality、Shadowsocks2022、Trojan、Hysteria2
- ⚡ **高性能** - 基于sing-box和xray双核心
- 🛡️ **安全可靠** - 支持Reality、TLS等安全传输
- 📊 **实时监控** - 流量统计、在线用户、节点状态
- 🔧 **易于部署** - 一键安装脚本，快速上手

## 🚀 快速安装

### 一键安装脚本

```bash
wget -N https://raw.githubusercontent.com/q42602736/V2BX-SSPanel-UIM/main/install.sh && bash install.sh
```

### 手动安装

1. **下载最新版本**
   ```bash
   wget https://github.com/q42602736/V2BX-SSPanel-UIM/releases/latest/download/V2bX-linux-64.zip
   ```

2. **解压并安装**
   ```bash
   unzip V2bX-linux-64.zip
   chmod +x V2bX
   sudo mv V2bX /usr/local/bin/
   ```

3. **配置文件**
   ```bash
   sudo mkdir -p /etc/V2bX
   sudo cp config.json /etc/V2bX/
   ```

## 📋 支持的架构

| 架构 | 文件名 | 状态 |
|------|--------|------|
| x86_64 | `V2bX-linux-64.zip` | ✅ 支持 |
| ARM64 | `V2bX-linux-arm64-v8a.zip` | ✅ 支持 |
| s390x | `V2bX-linux-s390x.zip` | ✅ 支持 |

## 🔧 配置说明

### 基础配置

```json
{
  "Nodes": [
    {
      "Core": "sing",
      "ApiHost": "https://your-panel.com",
      "ApiKey": "your-api-key",
      "NodeID": 1,
      "NodeType": "shadowsocks"
    }
  ]
}
```

### 支持的节点类型

- `shadowsocks` - Shadowsocks2022协议
- `vmess` - VMess协议
- `vless` - VLESS+Reality协议
- `trojan` - Trojan协议
- `hysteria2` - Hysteria2协议

## 📖 使用说明

### 管理命令

```bash
V2bX start        # 启动服务
V2bX stop         # 停止服务
V2bX restart      # 重启服务
V2bX status       # 查看状态
V2bX log          # 查看日志
V2bX update       # 更新版本
```

### 服务管理

```bash
# 设置开机自启
sudo systemctl enable V2bX

# 查看服务状态
sudo systemctl status V2bX

# 查看实时日志
sudo journalctl -u V2bX -f
```

## 🆚 与原版差异

| 功能 | 原版V2BX | 本项目 |
|------|----------|--------|
| SSPanel-UIM支持 | ❌ | ✅ |
| Shadowsocks2022 | ⚠️ 部分 | ✅ 完整 |
| VLESS+Reality | ⚠️ 部分 | ✅ 完整 |
| 订阅生成 | ❌ | ✅ |
| 多协议混合 | ❌ | ✅ |

## 🤝 贡献

欢迎提交Issue和Pull Request！

1. Fork本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

## 📄 许可证

本项目基于 [MIT License](LICENSE) 开源。

## 🙏 致谢

- [V2BX](https://github.com/wyx2685/V2bX) - 原始项目
- [SSPanel-UIM](https://github.com/Anankke/SSPanel-UIM) - 面板支持
- [sing-box](https://github.com/SagerNet/sing-box) - 核心引擎
- [Xray-core](https://github.com/XTLS/Xray-core) - 核心引擎

---

<div align="center">

**⭐ 如果这个项目对您有帮助，请给个Star支持一下！**

</div>
