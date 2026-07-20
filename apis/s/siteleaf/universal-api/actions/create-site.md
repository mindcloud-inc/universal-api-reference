# Siteleaf: Create Site

Creates a new site in Siteleaf.

```
POST https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Site domain |
| `title` | string | no | Site title |

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

Through the native Siteleaf API, this operation is `POST /sites` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

