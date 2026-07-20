# Dribbble: List User Shots



```
GET https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/list-user-shots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/list-user-shots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/list-user-shots?${params}`, {
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
      "animated": true,
      "attachments": [
        {}
      ],
      "description": "string",
      "height": 1,
      "htmlUrl": "https://example.com",
      "id": 1,
      "images": {},
      "lowProfile": true,
      "projects": [
        {}
      ],
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "team": {},
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "video": {},
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `animated` | boolean |  |
| `attachments` | array<object> |  |
| `description` | string |  |
| `height` | number |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `images` | object |  |
| `lowProfile` | boolean |  |
| `projects` | array<object> |  |
| `publishedAt` | date |  |
| `tags` | array<string> |  |
| `team` | object |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `video` | object |  |
| `width` | number |  |

## Native endpoint

Through the native Dribbble API, this operation is `GET /user/shots` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-shots.md) for the provider-specific parameters and requirements.

