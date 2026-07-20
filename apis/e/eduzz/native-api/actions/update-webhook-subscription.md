# Update Webhook Subscription with Eduzz

Updates an existing webhook subscription in Eduzz.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhook/v1/subscription/:subscriptionId`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Update Webhook Subscription](https://developers.eduzz.com/reference/api/put-webhook-v1-subscription-subscriptionId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Id da configuração. |
| `name` | body | `string` | no | Nome da inscrição. |
| `url` | body | `string` | no | URL do WebHook. |
| `events[]` | body | `array<object>` | no | Eventos que o WebHook irá receber. |
| `events[].name` | body | `string` | no | Nome do evento. |
| `filters[]` | body | `array<object>` | no | Filtros para os eventos. |
| `filters[].metadata` | body | `string` | no | Nome do filtro. |
| `filters[].values[]` | body | `array<string>` | no | Valores para o filtro. |
