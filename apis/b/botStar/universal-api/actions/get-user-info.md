# BotStar: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/botStar/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotStar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/get-user-info?connectionId=$CONNECTION_ID&botId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botStar/latest/actions/get-user-info?${params}`, {
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
| `userId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "2026-05-07T12:00:00.000Z",
      "board_id": "string",
      "channel": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "ip": "string",
      "last_name": "Chen",
      "locale": "string",
      "name": "Ava Chen",
      "otn_topics": [
        {
          "expired_at": 1,
          "id": "string",
          "name": "Ava Chen",
          "token": "string"
        }
      ],
      "picture": "string",
      "some_custom_attributes1": "string",
      "tags": [
        "string"
      ],
      "timezone": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | date |  |
| `board_id` | string |  |
| `channel` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `ip` | string |  |
| `last_name` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `otn_topics[].expired_at` | number |  |
| `otn_topics[].id` | string |  |
| `otn_topics[].name` | string |  |
| `otn_topics[].token` | string |  |
| `picture` | string |  |
| `some_custom_attributes1` | string |  |
| `tags[]` | string |  |
| `timezone` | number |  |

## Native endpoint

Through the native BotStar API, this operation is `GET /bots/:botId/users/:userId` (base URL `https://apis.botstar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

