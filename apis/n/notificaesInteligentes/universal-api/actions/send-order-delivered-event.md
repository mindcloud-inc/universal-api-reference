# Notificações Inteligentes: Send Order Delivered Event

Creates an order delivered event in Notificações Inteligentes.

```
POST https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/send-order-delivered-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notificações Inteligentes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/send-order-delivered-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "store": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/send-order-delivered-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "store": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `store` | string | yes | The integration store identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Notificações Inteligentes API, this operation is `POST /integrations/:store/events/order-delivered` (base URL `https://api.notificacoesinteligentes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-order-delivered-event.md) for the provider-specific parameters and requirements.

