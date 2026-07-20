# Circle: List Community Segments

Retrieves community segment records from Circle.

```
GET https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-community-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-community-segments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circle/latest/actions/list-community-segments?${params}`, {
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
      "audienceCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "publicUid": "string"
      },
      "id": 1,
      "rules": {
        "ruleType": "string"
      },
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceCount` | number |  |
| `createdAt` | date |  |
| `createdBy.avatarUrl` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | number |  |
| `createdBy.name` | string |  |
| `createdBy.publicUid` | string |  |
| `id` | number |  |
| `rules.ruleType` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Circle API, this operation is `GET /api/admin/v2/community_segments` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-community-segments.md) for the provider-specific parameters and requirements.

