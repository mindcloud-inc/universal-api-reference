# Notificações Inteligentes: Create Integration

Creates a new integration in Notificações Inteligentes.

```
POST https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/create-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notificações Inteligentes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/create-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "platform": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/create-integration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "platform": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Integration name. |
| `platform` | string | yes | Integration platform slug. |

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

Through the native Notificações Inteligentes API, this operation is `POST /integrations` (base URL `https://api.notificacoesinteligentes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-integration.md) for the provider-specific parameters and requirements.

