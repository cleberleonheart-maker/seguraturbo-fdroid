# SeguroTurbo — Repositório F-Droid

Repositório F-Droid **próprio** (alternativo) do app
[SeguroTurbo](https://github.com/cleberleonheart-maker/Seguroturbo).

O F-Droid oficial ainda não aceitou o app (política de 3 meses de manutenção),
então este repositório permite instalar e receber atualizações pelo app F-Droid.

## Como adicionar

1. Abra o **F-Droid** → **Configurações** → **Repositórios** → **+**
2. Cole a URL:

   ```
   https://cleberleonheart-maker.github.io/seguraturbo-fdroid/repo
   ```

3. Toque em **Adicionar** e depois **Atualizar**.
4. Procure por **SeguroTurbo** e instale.

## Verificação da assinatura

Confira se o repositório é legítimo pelo fingerprint da chave (SHA-256):

```
92:FB:1F:52:80:E4:F8:26:32:72:12:81:B0:BB:55:59:AC:D9:93:E7:FE:A0:7A:67:10:D5:3F:6C:97:6E:73:34
```

> **Atenção:** a chave do repositório foi regerada em 20/10/2026 (assinatura
> anterior removida). Se você já tinha adicionado este repositório, remova e
> adicione de novo para aceitar a nova chave.

## Atualizar o repositório

No projeto principal (segue `fdroid/gerar-repo.sh`):

```bash
# 1. baixe o APK oficial da release e coloque como com.seguraturbo.app_<versionCode>.apk
# 2. dentro de ~/fdroid-repo, com as senhas do keystore exportadas:
FDROID_KEY_STORE_PASS=... FDROID_KEY_PASS=... fdroid update -c
# 3. publique a pasta:
cp -r ~/fdroid-repo/repo/* <esta pasta>/repo/
```

A senha do keystore fica em `~/fdroid-repo/.keystore-pass` (nunca versionar).
