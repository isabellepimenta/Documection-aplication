# Notificador Microsoft Teams

## 📌 Visão Geral

O Notificador Microsoft Teams é uma biblioteca Python responsável por enviar mensagens para canais ou chats do Microsoft Teams utilizando Webhooks.

A aplicação recebe uma mensagem de texto, monta um payload no formato Adaptive Card e realiza uma requisição HTTP para o endpoint do Teams.

---

## 🎯 Objetivo

Automatizar notificações enviadas ao Microsoft Teams para comunicar:

- Sucesso de processos automatizados
- Falhas em execuções
- Alertas operacionais
- Status de integrações
- Monitoramento de sistemas
- Resultados de processamento

---

## ⚙️ Funcionamento

O fluxo da aplicação é simples:

1. Recebe uma mensagem.
2. Recebe a URL do Webhook do Teams.
3. Valida os parâmetros recebidos.
4. Monta um Adaptive Card.
5. Envia uma requisição HTTP POST.
6. Registra logs da operação.
7. Retorna o resultado do envio.

---

## 🏗 Arquitetura

```text
Sistema Origem
      |
      v
enviar_notificacao_teams()
      |
      v
Validação dos Dados
      |
      v
Montagem do Payload
      |
      v
Webhook Microsoft Teams
      |
      v
Canal Teams
