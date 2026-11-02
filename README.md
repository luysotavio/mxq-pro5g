# MXQ-Pro5G / Beelink X2 OpenWrt Firmware

Firmware personalizado para TV Box Beelink X2 (Allwinner H3, 4× Cortex-A7) com OpenWrt **SNAPSHOT**.

## Status

- ✅ USB Tethering (RNDIS) como WAN  
- ✅ NAT + DHCP + 5 GHz Wi-Fi  
- ✅ SSH key-only (dropbear, root via ed25519)  
- ✅ kmod-usb-net-rndis instalado  

## Arquivos

| Arquivo | Descrição |
|---------|-----------|
| `sdcard-p1p2.img` | Imagem completa do microSD (p1+p2, ~150 MB) |
| `overlay-backup.tar.gz` | Backup do overlay (`/overlay`) |

## Como restaurar

```bash
# Via sysupgrade (do LuCI ou SSH)
sysupgrade -n /tmp/sdcard-p1p2.img

# Via dd no PC
sudo dd if=sdcard-p1p2.img of=/dev/sdX bs=4M conv=fsync
```

## Credenciais

- **root SSH**: chave pública em `~/.ssh/box_rk322x.pub`
- **root LuCI**: senha gravada em `~/.beelinkx2-root-pass.txt`

## Changelog

- 2026-11-02: USB Tethering RNDIS configurado, Wi-Fi 5 GHz ativo

---

*Gerado automaticamente via OpenWrt builds*
