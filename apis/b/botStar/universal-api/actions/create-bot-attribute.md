# BotStar: Create Bot Attribute



```
POST https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-bot-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-bot-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string",
  "dataType": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botStar/latest/actions/create-bot-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string",
    "dataType": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes |  |
| `dataType` | string | yes |  |
| `desc` | string | no |  |
| `env` | string | no |  |
| `name` | string | yes |  |
| `value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_type": "string",
      "desc": "string",
      "id": "string",
      "name": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_type` | string |  |
| `desc` | string |  |
| `id` | string |  |
| `name` | string |  |
| `value` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `POST /bots/:botId/attributes` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot-attribute.md) for the provider-specific parameters and requirements.

