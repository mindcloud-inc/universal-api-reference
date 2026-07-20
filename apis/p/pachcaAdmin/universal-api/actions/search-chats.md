# Pachca (Admin): Search Chats

Finds chats in the Pachca Admin API by search query.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/search-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/search-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/search-chats?${params}`, {
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
| `active` | boolean | no | Filter by active chats. |
| `chatSubtype` | string | no | Filter by chat subtype. |
| `createdFrom` | date | no | Filter chats created on or after this timestamp. |
| `createdTo` | date | no | Filter chats created on or before this timestamp. |
| `cursor` | string | no | Pagination cursor from meta.paginate.next_page. |
| `limit` | number | no | Number of results to return. |
| `order` | string | no | Sort direction. |
| `personal` | boolean | no | Filter personal chats only. |
| `query` | string | no | Full-text search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "channel": true,
          "createdAt": {},
          "id": 1,
          "lastMessageAt": {},
          "meetRoomUrl": "https://example.com",
          "memberIds": [
            1
          ],
          "name": "Ava Chen",
          "ownerId": {},
          "personal": true,
          "public": true
        }
      ],
      "meta": {
        "paginate": {
          "nextPage": "string"
        },
        "total": 1
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
| `data[].createdAt` | object |  |
| `data[].id` | number |  |
| `data[].lastMessageAt` | object |  |
| `data[].meetRoomUrl` | string |  |
| `data[].memberIds[]` | number |  |
| `data[].name` | string |  |
| `data[].ownerId` | object |  |
| `data[].personal` | boolean |  |
| `data[].public` | boolean |  |
| `meta.paginate.nextPage` | string |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /search/chats` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-chats.md) for the provider-specific parameters and requirements.

