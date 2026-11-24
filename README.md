# Ynsra RPG - Passo a passo para criar o APK pelo GitHub

Criador: Vtzxxy | Versão v0.2

## O que tem neste pacote
- `www/index.html` - o aplicativo completo
- `package.json` e `capacitor.config.json` - configuração do app Android
- `.github/workflows/build-apk.yml` - receita que gera o APK automaticamente
- `assets/` - ícone do app (logo)
- `.gitignore`

## Passo a passo
1. Extraia o zip no seu aparelho ou computador.
2. Entre em github.com e faça login (crie uma conta grátis se precisar).
3. Toque em **+ > New repository**. Nome: `ynsra-rpg`. Deixe **Public** ou **Private** e toque em **Create repository**.
4. Toque em **uploading an existing file** (ou Add file > Upload files).
5. Envie o CONTEÚDO da pasta extraída (não o zip): `www`, `assets`, `package.json`, `capacitor.config.json`, `.gitignore`, `README.md`.
6. Toque em **Commit changes**.
7. A pasta oculta `.github` pode não subir pelo navegador. Para criar o workflow manualmente:
   - Add file > **Create new file**
   - No nome digite exatamente: `.github/workflows/build-apk.yml`
   - Cole o conteúdo do arquivo `build-apk.yml` que está dentro da pasta `.github/workflows` do zip
   - Commit changes
8. Abra a aba **Actions**. Se pedir, toque em para ativar os workflows.
9. Toque em **Build APK** > **Run workflow** > **Run workflow**.
10. Espere de 5 a 10 minutos até aparecer o ícone verde. Se ficar vermelho, abra a execução e copie a mensagem de erro.
11. Abra a execução concluída, role até **Artifacts** e baixe `ynsra-rpg-apk` (vem dentro de um zip: extraia).
12. Abra o `app-debug.apk` no Android e permita "instalar apps desconhecidos" quando o sistema pedir.

## Como atualizar
Edite ou substitua `www/index.html` no GitHub, faça commit e rode o workflow de novo (ele também roda sozinho a cada commit na branch `main`).

## Observações
- É um APK de teste (debug), ótimo para uso pessoal. Para a Play Store seria preciso gerar um APK de release assinado.
- O ícone do app é a sua logo (dados e ficha), gerada automaticamente a partir da pasta `assets`.
- Os dados ficam no aparelho. Faça backup em Configurações antes de desinstalar.
