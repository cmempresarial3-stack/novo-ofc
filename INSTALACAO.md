# 🚀 Guia de Instalação - Verso Diário

## ⚠️ IMPORTANTE

Este projeto foi transformado de uma aplicação web para **React Native/Expo**. O código está pronto para download e desenvolvimento local. **O Replit serve apenas como IDE/repositório**.

## 📋 Estado Atual do Projeto

### ✅ Implementado (Estrutura Base - 60%)

1. **Navegação Completa**
   - Expo Router configurado
   - Bottom tabs (5 abas principais)
   - Stack navigation funcionando
   - Rotas definidas

2. **Contextos Globais**
   - ThemeContext (modo claro/escuro)
   - UserContext (dados do usuário)
   - NotificationContext (notificações)

3. **Telas Principais**
   - ✅ Onboarding (primeira execução)
   - ✅ Home (verso do dia, devocionais, navegação)
   - ✅ Bíblia (lista de livros, busca, filtros)
   - ✅ Hinário (lista, busca)
   - ✅ Loja (produtos, design)
   - ✅ Configurações (perfil, tema, notificações)
   - ✅ Devocional Completo (leitura)

4. **Funcionalidades Base**
   - AsyncStorage para dados locais
   - Modo escuro/claro
   - Sistema de favoritos
   - Compartilhamento de versos
   - Upload de foto de perfil

### 🚧 Falta Implementar (40%)

1. **Leitura da Bíblia**
   - Visualização de capítulos e versículos
   - Text-to-Speech (TTS)
   - Marcar favoritos em versículos
   - Adicionar notas

2. **Player de Hinário**
   - Reprodução de áudio dos hinos
   - Letras sincronizadas
   - Controles de playback

3. **Telas Faltantes**
   - Anotações (criar, editar, listar)
   - Calendário (progresso espiritual)
   - Alarmes (configuração de horários)

4. **Integrações**
   - Redes sociais (links externos)
   - Loja (pagamento externo)
   - Sons de notificação personalizados

5. **Assets**
   - Ícones do app (placeholder criado)
   - Splash screen (placeholder criado)
   - Áudios dos hinos
   - Sons de notificação

## 🛠️ Como Instalar Localmente

### 1. Pré-requisitos

```bash
# Verificar Node.js (v18+)
node --version

# Instalar Expo CLI globalmente
npm install -g expo-cli

# Instalar Expo Go no celular
# Android: https://play.google.com/store/apps/details?id=host.exp.exponent
# iOS: https://apps.apple.com/app/expo-go/id982107779
```

### 2. Download do Código

**Opção A: Download direto do Replit**
1. Clique em "Download as ZIP"
2. Extraia para uma pasta local

**Opção B: Git Clone (se configurado)**
```bash
git clone [URL_DO_REPLIT]
cd verso-diario
```

### 3. Instalação de Dependências

```bash
# Instalar todas as dependências
npm install

# Se houver erro, limpar e reinstalar
rm -rf node_modules package-lock.json
npm install
```

### 4. Executar o App

```bash
# Iniciar o servidor Expo
npx expo start

# Ou
npm start
```

### 5. Ver no Celular

1. Abra o **Expo Go** no seu celular
2. Escaneie o QR code exibido no terminal
3. Aguarde o app carregar

## 📱 Gerar APK para Instalação

### Método 1: EAS Build (Recomendado)

```bash
# 1. Instalar EAS CLI
npm install -g eas-cli

# 2. Login no Expo
eas login

# 3. Configurar projeto
eas build:configure

# 4. Build APK
eas build --platform android --profile preview

# 5. Aguardar build (5-10 minutos)
# 6. Fazer download do APK gerado
# 7. Instalar no Android
```

### Método 2: Build Local

```bash
# 1. Gerar arquivos nativos
npx expo prebuild

# 2. Abrir no Android Studio
# Navegue até a pasta android/
# Abra o projeto

# 3. Build > Build Bundle(s) / APK(s) > Build APK(s)

# 4. APK estará em: android/app/build/outputs/apk/
```

## 🐛 Solução de Problemas

### Erro: "Unable to resolve module"

```bash
# Limpar cache e reinstalar
rm -rf node_modules
npm install
npx expo start --clear
```

### Erro: "SDK Version Mismatch"

```bash
# Atualizar Expo Go para SDK 51
# Ou executar:
npx expo install --fix
```

### APK não instala no Android

1. Ativar "Fontes desconhecidas" nas configurações
2. Verificar arquitetura do APK (ARM/x86)

### App fecha ao abrir

1. Verificar logs: `npx expo start`
2. Procurar erros no console
3. Verificar se assets existem (ícones, sons)

## 📁 Estrutura do Projeto

```
verso-diario/
├── app/                    # Telas (Expo Router)
│   ├── (tabs)/            # Navegação por tabs
│   ├── _layout.tsx        # Layout raiz
│   └── index.tsx          # Splash screen
├── contexts/              # Contextos React
├── data/                  # Dados (versos, bíblia, hinos)
├── assets/                # Imagens, sons, ícones
├── app.json               # Config do Expo
├── eas.json               # Config de build
└── package.json           # Dependências
```

## ✏️ Próximas Implementações Necessárias

Para completar o app conforme especificação original:

1. **Prioridade Alta**
   - Implementar leitura completa da Bíblia
   - Adicionar TTS (Text-to-Speech)
   - Criar tela de Anotações
   - Criar tela de Calendário
   - Player de áudio para hinário

2. **Prioridade Média**
   - Configuração de alarmes
   - Integração com redes sociais
   - Sistema completo de favoritos
   - Sincronização de dados

3. **Prioridade Baixa**
   - Pulseira QR/NFC
   - Estatísticas detalhadas
   - Conquistas e badges

## 📞 Suporte

Para dúvidas técnicas:
- Consulte a documentação do Expo: https://docs.expo.dev/
- React Native docs: https://reactnative.dev/

## 📄 Licença

Projeto pessoal e educacional.

---

🕊️ **Verso Diário** - Desenvolvido com React Native + Expo
