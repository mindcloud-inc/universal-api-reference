# Request Webhook Test with Eduzz

Requests a test delivery for an Eduzz webhook subscription.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/v1/subscription/sample`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Request Webhook Test](https://developers.eduzz.com/reference/api/post-webhook-v1-subscription-sample)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | body | `string` | no | Id da Configuração do WebHook. |
| `event` | body | `string` | no | Nome do evento. |
