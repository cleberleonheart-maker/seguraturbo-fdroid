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
E2:71:D8:A4:B1:18:18:1B:9B:9B:A1:37:55:E3:97:85:C4:72:14:39:9A:2D:8B:7D:42:2D:0E:D5:14:5C:98:F9
```

## Atualizar o repositório

No projeto principal:

```bash
./build.sh                       # gera o APK release assinado
cp app/build/outputs/apk/release/app-release.apk ~/fdroid-repo/repo/
cd ~/fdroid-repo && fdroid update -c
cp -r ~/fdroid-repo/repo/* <esta pasta>/repo/
```
