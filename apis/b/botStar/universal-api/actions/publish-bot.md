# BotStar: Publish Bot



```
PUT https://connect.mindcloud.co/v1/universal/botStar/latest/actions/publish-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/publish-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botStar/latest/actions/publish-bot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `POST /bots/:botId/publish` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-bot.md) for the provider-specific parameters and requirements.

