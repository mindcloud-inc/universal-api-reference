# BotStar: List Bot Attributes



```
GET https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-bot-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-bot-attributes?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-bot-attributes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes |  |
| `env` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "data_type": "string",
          "desc": "string",
          "id": "string",
          "name": "Ava Chen",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].data_type` | string |  |
| `[].desc` | string |  |
| `[].id` | string |  |
| `[].name` | string |  |
| `[].value` | string |  |

## Native endpoint

Through the native BotStar API, this operation is `GET /bots/:botId/attributes` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bot-attributes.md) for the provider-specific parameters and requirements.

