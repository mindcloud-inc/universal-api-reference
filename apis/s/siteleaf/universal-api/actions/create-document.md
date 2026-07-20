# Siteleaf: Create Document

Creates a new document in Siteleaf.

```
POST https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-document', {
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
| `collectionPath` | string | no | Collection path slug |
| `siteId` | string | no | Siteleaf site identifier |
| `title` | string | no | Document title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "basename": "Ava Chen",
      "body": "string",
      "categories": [
        "string"
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "defaults": {},
      "directory": "string",
      "filename": "Ava Chen",
      "id": "string",
      "metadata": {},
      "path": "string",
      "permalink": "https://example.com",
      "sha": "string",
      "site_id": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_id": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `basename` | string |  |
| `body` | string |  |
| `categories` | array<string> |  |
| `created_at` | date |  |
| `date` | date |  |
| `defaults` | object |  |
| `directory` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `path` | string |  |
| `permalink` | string |  |
| `sha` | string |  |
| `site_id` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `POST /sites/:site_id/collections/:path/documents` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

