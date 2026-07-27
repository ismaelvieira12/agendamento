# Gabriely Braga — Site de Agendamento 💄

Site de agendamento de sobrancelhas (Design simples e Design com henna) com
painel de administração para configurar tudo sem mexer no código.

## Recursos
- Layout mobile no estilo cartão de perfil (WhatsApp, Instagram, localização, horário)
- Lista de serviços com preço e duração
- Pop-up de agendamento com dias e horários disponíveis
- Confirmação enviada direto para o WhatsApp
- **Painel admin** (`admin.html`) protegido por login para configurar número, Instagram,
  local, serviços/valores e horários — clientes veem apenas a página pública

## Arquivos
- `index.html` — site público (só visualização)
- `admin.html` — painel de administração (login e senha)
- `firebase-config.js` — chaves do projeto Firebase (você preenche)
- `firestore.rules` — regras de segurança do banco (leitura pública, escrita só logado)

## Como publicar de graça (GitHub Pages)
1. No GitHub, vá em **Settings → Pages**
2. Em **Branch**, selecione `main` e a pasta `/ (root)` e salve
3. Site fica em `https://SEU-USUARIO.github.io/NOME-DO-REPO/`
   e o painel em `.../admin.html`

## Configurar o painel (Firebase — grátis)
1. Crie um projeto em https://console.firebase.google.com
2. **Firestore Database** → Criar banco (modo produção)
3. Na aba **Regras**, cole o conteúdo de `firestore.rules` e publique
4. **Authentication** → Sign-in method → ative **E-mail/senha**
5. Na aba **Users**, clique em **Adicionar usuário** e crie o login da dona
6. **Configurações do projeto** → seus apps → **App da Web** (`</>`) →
   copie o objeto de configuração para dentro de `firebase-config.js`
7. Pronto: acesse `admin.html`, faça login e configure. As mudanças aparecem
   para todos os clientes automaticamente.

> Enquanto o `firebase-config.js` estiver com os valores `COLE_...`, o site
> funciona normalmente usando os valores padrão embutidos no `index.html`.
