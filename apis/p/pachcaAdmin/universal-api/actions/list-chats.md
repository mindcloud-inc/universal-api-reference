# Pachca (Admin): List Chats

Retrieves chats from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-chats?${params}`, {
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
| `lastMessageAtAfter` | date | no | Filter chats whose last message was created on or after this timestamp. |
| `lastMessageAtBefore` | date | no | Filter chats whose last message was created on or before this timestamp. |
| `limit` | number | no |  |
| `order` | string | no | Sort direction. |
| `sort` | string | no | Sort field. |
| `cursor` | string | no |  |
| `personal` | boolean | no |  |
| `availability` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "channel": true,
          "createdAt": "string",
          "id": 1,
          "lastMessageAt": "string",
          "meetRoomUrl": "https://example.com",
          "memberIds": [
            1
          ],
          "name": "Ava Chen",
          "ownerId": 1,
          "personal": true,
          "public": true
        }
      ],
      "meta": {
        "paginate": {
          "nextPage": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].channel` | boolean |  |
| `data[].createdAt` | string |  |
| `data[].id` | number |  |
| `data[].lastMessageAt` | string |  |
| `data[].meetRoomUrl` | string |  |
| `data[].memberIds[]` | number |  |
| `data[].name` | string |  |
| `data[].ownerId` | number |  |
| `data[].personal` | boolean |  |
| `data[].public` | boolean |  |
| `meta.paginate.nextPage` | string |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /chats` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

