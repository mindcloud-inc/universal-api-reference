# Chatforma: List Open Dialog Users

Retrieves users with open dialogs from Chatforma.

```
GET https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-open-dialog-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-open-dialog-users?connectionId=$CONNECTION_ID&limit=25&offset=0&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/list-open-dialog-users?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": 1,
      "chatId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "id": 1,
      "lastMessageCreatedAt": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "message": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | number |  |
| `chatId` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastMessageCreatedAt` | date |  |
| `lastName` | string |  |
| `message` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Chatforma API, this operation is `GET /bots/:botId/dialogs/users` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-open-dialog-users.md) for the provider-specific parameters and requirements.

