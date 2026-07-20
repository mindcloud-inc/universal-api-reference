# ManyChat: Create Bot Field

Creates a new bot field in ManyChat.

```
POST https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/create-bot-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/create-bot-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/create-bot-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `type` | string | yes |  |
| `description` | string | no |  |
| `value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {
        "description": "string",
        "id": 1,
        "name": "Ava Chen",
        "type": "string",
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field.description` | string |  |
| `field.id` | number |  |
| `field.name` | string |  |
| `field.type` | string |  |
| `field.value` | string |  |

## Native endpoint

Through the native ManyChat API, this operation is `POST /fb/page/createBotField` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot-field.md) for the provider-specific parameters and requirements.

