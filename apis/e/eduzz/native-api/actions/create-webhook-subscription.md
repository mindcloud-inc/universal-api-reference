# Create Webhook Subscription with Eduzz

Creates a webhook subscription in Eduzz.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/v1/subscription`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Create Webhook Subscription](https://developers.eduzz.com/reference/api/post-webhook-v1-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Nome da inscrição. |
| `url` | body | `string` | no | URL do WebHook. |
| `events[]` | body | `array<object>` | no | Eventos que o WebHook irá receber. |
| `events[].name` | body | `string` | no | Nome do evento. |
| `filters[]` | body | `array<object>` | no | Filtros para os eventos. |
| `filters[].metadata` | body | `string` | no | Nome do filtro. |
| `filters[].values[]` | body | `array<string>` | no | Valores para o filtro. |
