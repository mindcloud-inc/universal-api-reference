# Botbaba: Get Bot User



```
GET https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-bot-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-bot-user?connectionId=$CONNECTION_ID&botUserId=1&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botUserId": "1",
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-bot-user?${params}`, {
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
| `botUserId` | number | yes | The Botbaba bot user identifier. |
| `botId` | number | yes | The Botbaba bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": 1,
      "botTags": [
        {}
      ],
      "botUserFields": [
        {}
      ],
      "botUserId": 1,
      "email": "ava@example.com",
      "gender": "string",
      "mobile": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | number |  |
| `botTags` | array<object> |  |
| `botUserFields` | array<object> |  |
| `botUserId` | number |  |
| `email` | string |  |
| `gender` | string |  |
| `mobile` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Botbaba API, this operation is `GET /api/GetBotUserById` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-user.md) for the provider-specific parameters and requirements.

