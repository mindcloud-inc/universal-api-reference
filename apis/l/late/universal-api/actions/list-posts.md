# Late: List Posts



```
GET https://connect.mindcloud.co/v1/universal/late/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/list-posts?${params}`, {
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
| `status` | list<string> | no | Filter posts by status. One of: `draft`, `failed`, `published`, `scheduled`. |
| `platform` | string | no | Filter posts by platform. |
| `profileId` | string | no | Filter posts by profile ID. |
| `createdBy` | string | no | Filter posts by creator ID. |
| `dateFrom` | date | no | Return posts created on or after this date. |
| `dateTo` | date | no | Return posts created on or before this date. |
| `includeHidden` | boolean | no | When true, include hidden posts. |
| `search` | string | no | Search posts by text content. |
| `sortBy` | list<string> | no | Sort order for results. One of: `created-asc`, `created-desc`, `platform`, `scheduled-asc`, `scheduled-desc`, `status`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "crosspostingEnabled": true,
      "Id": "string",
      "scheduledFor": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timezone": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Post body text. |
| `createdAt` | date | Creation timestamp. |
| `crosspostingEnabled` | boolean | Whether crossposting is enabled for the post. |
| `Id` | string | Zernio post identifier. |
| `scheduledFor` | date | Draft or scheduled timestamp returned by Zernio. |
| `status` | string | Post lifecycle status. |
| `timezone` | string | Timezone stored on the post. |
| `title` | string | Post title when provided. |
| `updatedAt` | date | Last update timestamp. |
| `visibility` | string | Post visibility setting. |

## Native endpoint

Through the native Late API, this operation is `GET /posts` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

