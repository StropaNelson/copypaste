# CopyPaste - Compartilhe Texto P2P

Um site simples para compartilhar texto entre dois navegadores sem necessidade de backend.

## 🎯 Como Usar

1. Abra o site em dois navegadores diferentes (pode ser em diferentes PCs, celulares, etc)
2. Um usuário clica em "Ver ID completo" e copia o ID inteiro
3. O outro usuário cola o ID completo no campo "Cole o código/ID do outro usuário"
4. Clica em "Conectar"
5. Quando conectado, podem enviar textos entre si

## 🚀 Deploy no Netlify

### Opção 1: Deploy Automático (Recomendado)

1. Faça login no [Netlify](https://netlify.com)
2. Clique em "Add new site" → "Import an existing project"
3. Escolha GitHub como provedor
4. Selecione o repositório `copypaste`
5. Deixe as configurações padrão
6. Clique em "Deploy site"

**Pronto!** O site será deployado automaticamente a cada push para main.

### Opção 2: Deploy Manual

```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod --dir=.
```

## 🔧 Como Funciona

- **PeerJS**: Biblioteca para conexão P2P entre navegadores
- **WebRTC**: Tecnologia para comunicação direta entre navegadores
- **TURN/STUN Servers**: Servidores para funcionar em redes restritivas

## ⚠️ Melhorias para Redes Restritivas

Adicionei:
- ✅ Múltiplos servidores STUN
- ✅ Servidor TURN gratuito (metered.ca)
- ✅ Retry automático de conexão
- ✅ Debug logging para diagnóstico
- ✅ Validação de ID completo

## 📝 Tecnologias

- HTML5, CSS3, JavaScript Vanilla
- PeerJS (wrapper WebRTC)
- TURN Server Gratuito
