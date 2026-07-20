# Botbaba: Get Bot Widget Settings



```
GET https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-bot-widget-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-bot-widget-settings?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-bot-widget-settings?${params}`, {
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
| `botId` | number | yes | The Botbaba bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Botbaba API, this operation is `GET /api/GetBotWidgetSettings` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-widget-settings.md) for the provider-specific parameters and requirements.

