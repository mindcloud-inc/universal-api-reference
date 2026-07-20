# Circle: List Member Tags

Retrieves member tag records from Circle.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-member-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-member-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-member-tags?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customEmojiDarkUrl": "https://example.com",
      "customEmojiUrl": "https://example.com",
      "displayFormat": "string",
      "displayLocations": "string",
      "emoji": "string",
      "id": 1,
      "isBackgroundEnabled": true,
      "isPublic": true,
      "name": "Ava Chen",
      "taggedMembersCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `customEmojiDarkUrl` | string |  |
| `customEmojiUrl` | string |  |
| `displayFormat` | string |  |
| `displayLocations` | string |  |
| `emoji` | string |  |
| `id` | number |  |
| `isBackgroundEnabled` | boolean |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `taggedMembersCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/member_tags` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-member-tags.md) for the provider-specific parameters and requirements.

