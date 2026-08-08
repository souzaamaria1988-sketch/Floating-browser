# 🚀 Floating Browser - Android APK Build

Este projeto contém um **navegador flutuante** completo que pode ser compilado como um aplicativo Android (APK) usando GitHub Actions.

## 📱 Funcionalidades do App

- 🌐 Navegador WebView completo com JavaScript habilitado
- 🎨 Interface flutuante e dinâmica (do arquivo HTML original)
- 📱 Suporte a gestos, touch e zoom
- 🔒 Permissões de câmera, microfone e localização
- 📂 Gerenciador de favoritos e histórico
- ⌨️ Atalhos de teclado
- 🔄 Navegação completa (voltar, avançar, atualizar)
- 🎯 Barra de endereços funcional
- 📍 Suporte a geolocalização
- 🎥 Suporte a vídeo e áudio HTML5

## 🛠️ Como Compilar via GitHub Actions

### Opção 1: Build Automático (Push)

O build será executado automaticamente quando você:
- Fazer push para as branches `main` ou `develop`
- Criar um pull request para `main`
- Criar uma tag no formato `v*` (ex: `v1.0.0`)

### Opção 2: Build Manual (Workflow Dispatch)

1. Vá até a aba **Actions** no seu repositório GitHub
2. Selecione o workflow **"Build Android APK"**
3. Clique em **"Run workflow"**
4. Escolha a branch desejada
5. Clique em **"Run workflow"** novamente

### Opção 3: Release com Tag

Para criar uma release oficial:

```bash
# No seu terminal local
git tag v1.0.0
git push origin v1.0.0
```

Isso irá:
- Criar um build de release
- Publicar automaticamente no GitHub Releases
- Disponibilizar o APK para download

## 📦 Estrutura do Projeto Android

```
android/
├── app/
│   ├── build.gradle              # Configurações do app
│   ├── proguard-rules.pro        # Regras de ofuscação
│   └── src/main/
│       ├── AndroidManifest.xml   # Manifesto do app
│       ├── java/com/floatingbrowser/app/
│       │   └── MainActivity.java # Activity principal
│       ├── assets/
│       │   └── index.html        # Seu navegador HTML
│       └── res/                  # Recursos (layouts, temas, etc.)
├── build.gradle                  # Configurações do projeto
├── settings.gradle               # Configurações do Gradle
├── gradle.properties             # Propriedades do Gradle
├── gradlew                       # Script Unix
├── gradlew.bat                   # Script Windows
└── gradle/wrapper/
    └── gradle-wrapper.properties # Versão do Gradle
```

## 📥 Download do APK

Após o build ser concluído:

1. Vá até a aba **Actions** no GitHub
2. Clique no workflow concluído (✅)
3. Role até a seção **Artifacts**
4. Baixe o arquivo ZIP contendo o APK
5. Extraia e instale no seu dispositivo Android

## 🔧 Requisitos do Sistema

- **Android Minimum:** 5.0 (API 21)
- **Android Target:** 14 (API 34)
- **Java:** 17
- **Gradle:** 8.2
- **Android SDK:** 34

## 📋 Permissões Requeridas

O app solicita as seguintes permissões:
- 🌐 Internet e rede
- 📍 Localização (GPS)
- 📷 Câmera
- 🎤 Microfone
- 💾 Armazenamento

## 🚀 Próximos Passos

1. **Personalize o ícone:** Substitua os arquivos em `res/mipmap-*`
2. **Altere o package name:** Modifique em `build.gradle` e `AndroidManifest.xml`
3. **Assine o APK:** Para publicar na Play Store, configure a assinatura
4. **Habilite ProGuard:** Para ofuscação em release

## 🆘 Troubleshooting

### Build falha no GitHub Actions
- Verifique se todos os arquivos estão no repositório
- Confirme que o caminho `android/` está correto
- Veja os logs do workflow para detalhes do erro

### APK não instala
- Habilite "Fontes desconhecidas" nas configurações do Android
- Verifique se o APK não está corrompido
- Teste em um emulador primeiro

### WebView não carrega
- Verifique permissões de internet no manifesto
- Confirme que o arquivo `index.html` está em `assets/`

## 📄 Licença

Este projeto é open source e pode ser modificado conforme necessário.

---

**Desenvolvido com ❤️ para Floating Browser**
