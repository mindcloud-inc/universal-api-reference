# JANDI: Native API Reference

A consolidated summary of JANDI's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://support.jandi.com/en/categories/Connect-3c9dda43
- **API base URL:** `https://wh.jandi.com`

## Authentication

### Incoming Webhook

Store the JANDI incoming webhook URL generated in JANDI Connect.

### Credentials

- **Incoming Webhook URL:** `incomingWebhookUrl` · required · Paste the JANDI incoming webhook URL generated for the target chat room.

[Official authentication documentation](https://support.jandi.com/en/articles/Receiving-Incoming-Webhooks-in-JANDI-56bacd47)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.tosslab.jandi-v2+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Incoming Webhook Message](actions/send-incoming-webhook-message.md) | `POST {{credentials.incomingWebhookUrl}}` | [docs](https://support.jandi.com/en/articles/Receiving-Incoming-Webhooks-in-JANDI-56bacd47) |
