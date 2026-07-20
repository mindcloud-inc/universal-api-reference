# Sendbird: Get Bot



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-bot?connectionId=$CONNECTION_ID&botUserid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botUserid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-bot?${params}`, {
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
| `botUserid` | string | yes | The bot's user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botNickname": "Ava Chen",
      "botUserid": "string",
      "isEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botNickname` | string |  |
| `botUserid` | string |  |
| `isEnabled` | boolean |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /bots/:botUserid` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot.md) for the provider-specific parameters and requirements.

