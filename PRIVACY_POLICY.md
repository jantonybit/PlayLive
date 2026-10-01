# Política de Privacidade — PlayLive

**Última atualização:** 30 de setembro de 2026

---

## 1. Resumo

O PlayLive não coleta, transmite, armazena em servidores nem compartilha qualquer
dado pessoal. O aplicativo funciona inteiramente offline no computador do usuário.

---

## 2. Dados armazenados localmente

O PlayLive salva exclusivamente no computador do usuário:

| Dado | Local |
|---|---|
| Configurações e cenas | `%APPDATA%\PlayLive\` |
| Log técnico | `%APPDATA%\PlayLive\playlive.log` |
| Última cena utilizada | `~\.playlive_last_scene.json` |

Nenhum desses dados é transmitido a servidores ou a terceiros. O usuário pode
apagá-los a qualquer momento simplesmente excluindo esses arquivos.

---

## 3. Áudio

O aplicativo apenas **reproduz** arquivos de áudio que o usuário seleciona
explicitamente.

- Nenhum arquivo de áudio é enviado, compartilhado ou reprocessado remotamente.
- O aplicativo **não possui capacidade de captura de microfone**. A capability
  `microphone` não é declarada no pacote do aplicativo.
- O aplicativo não grava áudio.

---

## 4. Verificação de licença

A verificação da licença é realizada por meio da API local do Microsoft Store
(`Windows.Services.Store`). Este processo é executado pelo sistema operacional e
não envolve o desenvolvedor. Nenhum dado do usuário é transmitido ao
desenvolvedor.

O resultado da verificação (ativo, em teste ou expirado) é registrado apenas no
log técnico local.

---

## 5. Rede

O aplicativo:

- **não possui funcionalidade de rede**;
- não navega na web;
- não se comunica com servidores do desenvolvedor;
- não contém anúncios;
- não contém telemetria, rastreamento ou SDKs de analytics;
- não realiza upload nem download de arquivos do usuário.

A única URL externa presente no aplicativo aponta para a página oficial do
PlayLive na Microsoft Store e para as páginas de suporte e privacidade, e só é
aberta a pedido explícito do usuário.

---

## 6. Crianças

O aplicativo não é direcionado a crianças e não coleta dados de menores de
idade.

---

## 7. Direitos do usuário

Por não haver coleta, armazenamento ou compartilhamento de dados, não existem
dados pessoais sobre o usuário que possam ser objeto de solicitação de acesso,
correção, portabilidade ou exclusão.

O usuário tem controle total sobre seus dados locais, podendo exclu-los a
qualquer momento.

---

## 8. Permissões do sistema

O aplicativo declara apenas a capacidade `runFullTrust`, necessária para acessar
as APIs de áudio (WASAPI), MIDI (WinMM) e de arquivos do Windows. Nenhuma
permissão de câmera, microfone, localização, contatos ou calendário é solicitada.

---

## 9. Alterações nesta política

Eventuais atualizações desta política serão publicadas neste mesmo endereço. A
data da última atualização é indicada no início do documento.

---

## 10. Contato

Dúvidas sobre privacidade ou sobre este aplicativo:

**jantonybit@gmail.com**

Repositório público do projeto:
https://github.com/jantonybit/PlayLive
