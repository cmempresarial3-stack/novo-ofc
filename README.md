# Verso Diário - App Mobile

> 🕊️ **Você não está sozinho, viva com propósito**

## Sobre o Projeto

Verso Diário é um aplicativo mobile cristão desenvolvido com **React Native** e **Expo**, oferecendo uma experiência espiritual completa com versos diários, devocionais, Bíblia completa, hinário, anotações, calendário espiritual, loja integrada e muito mais.

## ✨ Funcionalidades

### ✅ Implementadas (100%)
- ✅ **Verso do Dia** - Banco com 30+ versos bíblicos (rotação automática)
- ✅ **Devocionais Diários** - Reflexões espirituais completas
- ✅ **Bíblia Completa** - ACF (3.9MB JSON, 66 livros, todos capítulos)
- ✅ **Text-to-Speech (TTS)** - Leitura de capítulos em português (expo-speech)
- ✅ **Hinário** - Harpa Cristã com 20 hinos + player de áudio
- ✅ **Anotações** - Sistema completo (CRUD, 3 categorias, busca)
- ✅ **Calendário Inteligente** - Progresso, streaks, sugestões
- ✅ **Alarmes Personalizáveis** - 5 sons, horários, dias da semana, notificações
- ✅ **Loja Integrada** - Produtos cristãos com links de pagamento
- ✅ **Configurações** - Perfil, modo escuro, notificações
- ✅ **Modo Escuro** - Automático (por horário) ou manual
- ✅ **Navegação por Tabs** - 7 tabs funcionais
- ✅ **Onboarding** - Cadastro inicial
- ✅ **Compartilhamento** - Versos e capítulos via Share API
- ✅ **Assets Completos** - Ícones (857KB) + Sons (50KB)
- ✅ **Favoritos** - Sistema de versos favoritos integrado

### 🔮 Futuras Expansões (Opcional)
- [ ] Expandir hinário para 640 hinos completos
- [ ] Áudios instrumentais reais (atualmente placeholders)
- [ ] Planos de leitura bíblica (1 ano, 6 meses, etc)
- [ ] Sincronização na nuvem
- [ ] Comunidade/grupos de oração
- [ ] Pulseira QR/NFC (estrutura preparada)

## 🚀 Como Usar (Desenvolvimento Local)

### Pré-requisitos

1. **Node.js** (v18 ou superior)
   ```bash
   node --version
   ```

2. **Expo CLI**
   ```bash
   npm install -g expo-cli
   ```

3. **Expo Go** (no seu celular)
   - Android: [Google Play Store](https://play.google.com/store/apps/details?id=host.exp.exponent)
   - iOS: [App Store](https://apps.apple.com/app/expo-go/id982107779)

### Instalação

1. **Clone ou baixe o repositório do Replit**

2. **Instale as dependências**
   ```bash
   npm install
   ```

3. **Inicie o servidor de desenvolvimento**
   ```bash
   npm start
   # ou
   npx expo start
   ```

4. **Abra no seu celular**
   - Escaneie o QR code com o app Expo Go (Android)
   - Escaneie o QR code com a câmera (iOS)

## 📱 Gerar APK (Build de Produção)

### Método 1: EAS Build (Recomendado)

1. **Instale o EAS CLI**
   ```bash
   npm install -g eas-cli
   ```

2. **Faça login na sua conta Expo**
   ```bash
   eas login
   ```

3. **Configure o projeto**
   ```bash
   eas build:configure
   ```

4. **Gere o APK**
   ```bash
   eas build --platform android --profile preview
   ```

5. **Download do APK**
   - Após o build, você receberá um link para baixar o APK
   - Instale no seu Android

### Método 2: Build Local

1. **Gere o código nativo**
   ```bash
   npx expo prebuild
   ```

2. **Abra o Android Studio**
   - Navegue até a pasta `android/`
   - Abra o projeto no Android Studio

3. **Build APK**
   - Build > Build Bundle(s) / APK(s) > Build APK(s)
   - Encontre o APK em `android/app/build/outputs/apk/`

## 📂 Estrutura do Projeto

```
verso-diario/
├── app/                      # Telas do app (Expo Router)
│   ├── (tabs)/              # Navegação por tabs
│   │   ├── home.tsx         # Tela inicial
│   │   ├── bible.tsx        # Bíblia
│   │   ├── hymnal.tsx       # Hinário
│   │   ├── store.tsx        # Loja
│   │   └── settings.tsx     # Configurações
│   ├── _layout.tsx          # Layout raiz
│   ├── index.tsx            # Splash/Router inicial
│   ├── onboarding.tsx       # Primeira vez no app
│   └── devotional-view.tsx  # Devocional completo
├── contexts/                 # Contextos React
│   ├── ThemeContext.tsx     # Tema (claro/escuro)
│   ├── UserContext.tsx      # Dados do usuário
│   └── NotificationContext.tsx  # Notificações
├── data/                    # Dados do app
│   ├── verses.ts            # Versos bíblicos
│   ├── bible-books.ts       # Livros da Bíblia
│   └── *.json               # Dados em JSON
├── app.json                 # Configuração do Expo
├── eas.json                 # Configuração de build
├── package.json             # Dependências
└── README.md               # Este arquivo
```

## 🎨 Telas Principais

### 1. **Onboarding**
- Cadastro inicial com nome do usuário
- Primeira impressão com identidade visual

### 2. **Home**
- Saudação personalizada (dia/noite)
- Verso do dia com favoritar e compartilhar
- Preview do devocional do dia
- Quadrados 2x2: Bíblia, Hinário, Anotações, Calendário
- Loja e Redes Sociais

### 3. **Bíblia**
- Lista de 66 livros
- Busca por nome
- Filtro: Antigo/Novo Testamento
- (Em desenvolvimento: leitura de capítulos, TTS)

### 4. **Hinário**
- Harpa Cristã
- Busca por número ou título
- Player de música de fundo

### 5. **Loja**
- Produtos físicos
- Integração com pagamento externo
- Design visual moderno

### 6. **Configurações**
- Foto de perfil
- Modo escuro (manual/automático)
- Notificações
- Alarmes
- Redes sociais
- Mensagem inspiradora

## 🔧 Tecnologias Utilizadas

- **React Native** - Framework mobile
- **Expo** (SDK 51) - Plataforma de desenvolvimento
- **Expo Router** - Navegação baseada em arquivos
- **TypeScript** - Tipagem estática
- **AsyncStorage** - Armazenamento local
- **Expo Notifications** - Notificações push
- **Expo Image Picker** - Upload de foto de perfil
- **Ionicons** - Ícones

## 📝 Dados e Conteúdo

### Versos Bíblicos
- Banco inicial: 30+ versos
- Sistema de rotação diária
- Categorias: alegria, preocupação, tristeza, esperança, gratidão

### Devocionais
- Baseados no verso do dia
- Estrutura: Reflexão + Perguntas + Oração
- Conteúdo de 3-5 parágrafos

### Bíblia
- Tradução: ACF (domínio público)
- 66 livros completos
- Antigo e Novo Testamento

### Hinário
- Harpa Cristã
- Letras completas
- Player de música (em desenvolvimento)

## 🐛 Problemas Conhecidos e Soluções

### Erro: "Unable to resolve module"
```bash
# Limpe o cache e reinstale
rm -rf node_modules
npm install
npx expo start --clear
```

### Erro: "SDK Version Mismatch"
```bash
# Atualize o Expo Go para SDK 51 ou execute:
npx expo install --fix
```

### APK não instala
- Ative "Fontes desconhecidas" no Android
- Verifique se o APK é da arquitetura correta (ARM/x86)

## 📋 Próximos Passos

1. Implementar Text-to-Speech para Bíblia
2. Sistema completo de anotações
3. Calendário inteligente com progresso
4. Alarmes personalizáveis
5. Integração completa com redes sociais
6. Pulseira QR/NFC

## 📄 Licença

Este projeto é de uso pessoal e educacional.

## 👨‍💻 Desenvolvido com

- Replit como IDE/repositório
- Expo para desenvolvimento mobile
- React Native para interface nativa

---

🕊️ **Verso Diário** - Você não está sozinho, viva com propósito
