# Chatforma: List Bot Users

Retrieves bot user records from Chatforma.

```
GET https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-bot-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-bot-users?connectionId=$CONNECTION_ID&limit=25&offset=0&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-bot-users?${params}`, {
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
| `botId` | number | yes |  |
| `deleted` | number | no | Set to show only deleted users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatId` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |

## Native endpoint

Through the native Chatforma API, this operation is `GET /bots/:botId/users` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bot-users.md) for the provider-specific parameters and requirements.

