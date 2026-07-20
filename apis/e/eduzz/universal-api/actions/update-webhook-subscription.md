# Eduzz: Update Webhook Subscription

Updates an existing webhook subscription in Eduzz.

```
PUT https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/update-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/update-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/update-webhook-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes | Id da configuração. |
| `name` | string | no | Nome da inscrição. |
| `url` | string | no | URL do WebHook. |
| `events[]` | array<object> | no | Eventos que o WebHook irá receber. |
| `events[].name` | string | no | Nome do evento. |
| `filters[]` | array<object> | no | Filtros para os eventos. |
| `filters[].metadata` | string | no | Nome do filtro. |
| `filters[].values[]` | array<string> | no | Valores para o filtro. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `PUT /webhook/v1/subscription/:subscriptionId` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-subscription.md) for the provider-specific parameters and requirements.

