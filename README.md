# Raízes da Fê

Aplicativo cristão para devocionais, oração, estudos e acesso à Bíblia NVI online.

## Identidade

- **Nome:** Raízes da Fê
- **Criador:** Bruno
- **Assinatura exibida:** “Feito com carinho por Bruno”
- **Pacote Android:** `br.com.presenca.app`
- **Orientação:** retrato
- **Tecnologia da interface:** HTML, CSS e JavaScript embarcados em Android WebView
- **Idioma:** português brasileiro

## Funcionalidades

- Palavra para hoje e reflexões guiadas.
- Registro de sentimentos e caminhada espiritual.
- Devocionais diários.
- Área de estudos com busca e categorias.
- Orações salvas e diário de oração.
- Planos de leitura.
- Exportação e importação de dados locais em JSON.
- Alternância entre modo claro e escuro.
- Alto contraste.
- Fonte para acessibilidade/dislexia.
- Remoção dos dados locais pelo próprio usuário.
- Assinatura visual do criador no rodapé.

## Bíblia NVI online

A Bíblia NVI não é armazenada dentro do aplicativo. A seção Bíblia abre a leitura online no navegador Android para respeitar os direitos autorais da tradução.

- **Antigo Testamento:** https://www.bibliaonline.com.br/nvi/gn
- **Novo Testamento:** https://www.bibliaonline.com.br/nvi/mt

O APK possui permissão de Internet e uma implementação nativa de `WebViewClient` que encaminha URLs HTTP/HTTPS para o navegador do aparelho.

## Navegação

A barra inferior contém apenas:

1. Início
2. Hoje
3. Bíblia
4. Orações

As configurações ficam exclusivamente no ícone de engrenagem do cabeçalho superior.

## Configurações

A tela de configurações foi organizada nas seções:

- **Aparência:** modo escuro.
- **Acessibilidade:** fonte para dislexia e alto contraste.
- **Dados locais:** exportação e importação de dados.
- **Zona de cuidado:** remoção dos dados locais.

A tela possui cartões, ícones, botões de estado, espaçamento responsivo, cabeçalho resumido e confirmação visual de salvamento automático.

## Design e experiência

- Identidade visual em azul profundo, branco e dourado.
- Layout responsivo para telas de celular.
- Espaços verticais reduzidos para evitar áreas vazias excessivas.
- Rodapé compacto com crédito do criador.
- Cabeçalho fixo com busca, tema e configurações.
- Navegação inferior fixa com quatro áreas principais.

## Arquivos principais

- `app/presenca.html`: interface, estilos, dados e lógica do app.
- `android/AndroidManifest.xml`: manifesto, pacote e permissão de Internet.
- `android/smali_classes2/br/com/presenca/app/MainActivity.smali`: Activity Android e WebView.
- `android/smali_classes2/br/com/presenca/app/ExternalWebViewClient.smali`: abertura nativa de links externos.
- `releases/RAIZES-DA-FE-COMPACTO.apk`: APK instalável assinado.

## Instalação

1. Baixe o arquivo APK.
2. Abra-o em um aparelho Android.
3. Caso solicitado, permita instalação de fontes desconhecidas para o aplicativo usado para abrir o APK.
4. Instale e abra **Raízes da Fê**.
5. Use o ícone de engrenagem no topo para acessar as configurações.

## Compilação local

O projeto original foi recompilado com Apktool e assinado com Uber APK Signer:

```bash
java -jar apktool.jar b android-decoded -o app-unsigned.apk
java -jar uber-apk-signer.jar --apks app-unsigned.apk --out signed --allowResign
```

O APK entregue foi alinhado, assinado e verificado com as assinaturas Android v1, v2 e v3.

## Versão entregue

- **Arquivo:** `RAIZES-DA-FE-COMPACTO.apk`
- **Tamanho aproximado:** 1,7 MB
- **Assinatura:** Android Debug keystore usada para esta compilação distribuível de teste
- **Estado:** APK recompilado, assinado e validado

> Para publicação na Google Play, deve ser usada uma chave de assinatura própria e um processo de build de produção.
