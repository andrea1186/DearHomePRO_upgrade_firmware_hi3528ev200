# Release Checklist Firmware

1. Build firmware custom valido (`openipc.hi3518ev200-nor-lite.custom.tgz`).
2. Verifica hash locale (`sha256sum`).
3. Crea o aggiorna release GitHub tag `latest`.
4. Carica asset con nome esatto:
   - `openipc.hi3518ev200-nor-lite.custom.tgz`
5. Test download URL pubblico:
   - `https://github.com/andrea1186/DearHomePRO_upgrade_firmware_hi3528ev200/releases/download/latest/openipc.hi3518ev200-nor-lite.custom.tgz`
6. Test update camera:
   - `sysupgrade -z --url "$(fw_printenv -n upgrade)" -k -r`
7. Smoke test camera post-reboot (rtsp, ssh, tunnel remoto).
