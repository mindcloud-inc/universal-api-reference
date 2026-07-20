# <img src="https://images.mindcloud.co/apps/icons/ai-wifi_1776880874650.png" alt="AiWifi logo" width="28" height="28"> AiWifi: Universal API

AiWifi: Manage AiWifi webhook configurations, test webhook deliveries, and inspect webhook delivery logs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aiWifi/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.aiwifi.io
- **Vendor API docs:** https://help.aiwifi.io/en/category/webhook

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get webhook events](actions/get-webhook-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/get-webhook-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get auth token](actions/get-auth-token.md) | POST |  |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get webhook log](actions/get-webhook-log.md) | GET | Retrieves details for a webhook delivery log in AiWifi. |
| [List webhook logs](actions/list-webhook-logs.md) | GET | Retrieves webhook delivery logs from AiWifi. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create webhook](actions/create-webhook.md) | POST | Creates a new webhook configuration in AiWifi. |
| [Delete webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook configuration from AiWifi. |
| [List webhooks](actions/list-webhooks.md) | GET | Retrieves webhook configurations from AiWifi. |
| [Set webhook enabled](actions/set-webhook-enabled.md) | PUT | Updates whether a webhook is active in AiWifi. |
| [Update webhook](actions/update-webhook.md) | PUT | Updates an existing webhook configuration in AiWifi. |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [Get webhook events](actions/get-webhook-events.md) | GET | Retrieves available webhook event types from AiWifi. |
| [Send test webhook event](actions/send-test-webhook-event.md) | POST | Sends a test event to a webhook in AiWifi. |

