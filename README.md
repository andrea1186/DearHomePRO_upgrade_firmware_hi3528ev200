# DearHome Firmware Updates (HI3518EV200)

Repository pubblico dedicato agli aggiornamenti firmware DearHome.

## Percorso update ufficiale

URL base release:

`https://github.com/andrea1186/DearHomePRO_upgrade_firmware_hi3528ev200/releases/download`

Asset firmware atteso da camera/app:

`openipc.hi3518ev200-nor-lite.custom.tgz`

URL consigliato (tag versione):

`https://github.com/andrea1186/DearHomePRO_upgrade_firmware_hi3528ev200/releases/download/vX.Y.Z/openipc.hi3518ev200-nor-lite.custom.tgz`

## Strategia consigliata per URL stabile

Per evitare di cambiare URL in campo a ogni release, usa sempre il tag `latest`:

`https://github.com/andrea1186/DearHomePRO_upgrade_firmware_hi3528ev200/releases/download/latest/openipc.hi3518ev200-nor-lite.custom.tgz`

Operativamente:
- mantieni una release/tag `latest`
- sostituisci l'asset `.tgz` a ogni nuova build validata

## Camera (OpenIPC)

Impostazione endpoint update:

```sh
fw_setenv upgrade "https://github.com/andrea1186/DearHomePRO_upgrade_firmware_hi3528ev200/releases/download/latest/openipc.hi3518ev200-nor-lite.custom.tgz"
```

Verifica:

```sh
fw_printenv -n upgrade
```

## Note

- Non committare i binari firmware nel repository git.
- Carica i `.tgz` come asset delle GitHub Release.
- Mantieni il nome file asset invariato per compatibilita con app/firmware.
