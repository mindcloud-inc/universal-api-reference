# Siteleaf: List Sites

Retrieves sites from Siteleaf.

```
GET https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-sites?${params}`, {
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
      "cname": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "defaults": [
        [
          {}
        ]
      ],
      "domain": "string",
      "id": "string",
      "jobs": {
        "preview": {
          "id": "string",
          "last_at": "2026-05-07T12:00:00.000Z",
          "last_error": "string",
          "last_id": "string"
        },
        "publish": {
          "id": "string",
          "last_at": "2026-05-07T12:00:00.000Z",
          "last_error": "string",
          "last_id": "string"
        },
        "sync": {
          "id": "string",
          "last_at": "2026-05-07T12:00:00.000Z",
          "last_error": "string",
          "last_id": "string"
        }
      },
      "metadata": {},
      "storage_limit": 1,
      "storage_used": 1,
      "timezone": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cname` | string |  |
| `created_at` | date |  |
| `defaults[]` | array<object> |  |
| `domain` | string |  |
| `id` | string |  |
| `jobs.preview.id` | string |  |
| `jobs.preview.last_at` | date |  |
| `jobs.preview.last_error` | string |  |
| `jobs.preview.last_id` | string |  |
| `jobs.publish.id` | string |  |
| `jobs.publish.last_at` | date |  |
| `jobs.publish.last_error` | string |  |
| `jobs.publish.last_id` | string |  |
| `jobs.sync.id` | string |  |
| `jobs.sync.last_at` | date |  |
| `jobs.sync.last_error` | string |  |
| `jobs.sync.last_id` | string |  |
| `metadata` | object |  |
| `storage_limit` | number |  |
| `storage_used` | number |  |
| `timezone` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `GET /sites` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

