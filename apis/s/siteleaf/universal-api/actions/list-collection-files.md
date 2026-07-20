# Siteleaf: List Collection Files

Retrieves collection files from Siteleaf.

```
GET https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-collection-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-collection-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-collection-files?${params}`, {
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
| `collectionPath` | string | no | Collection path slug |
| `siteId` | string | no | Siteleaf site identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "basename": "Ava Chen",
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "directory": "string",
      "download_url": "https://example.com",
      "edited_by_id": "string",
      "filename": "Ava Chen",
      "filesize": 1,
      "sha": "string",
      "site_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `basename` | string |  |
| `content_type` | string |  |
| `created_at` | date |  |
| `directory` | string |  |
| `download_url` | string |  |
| `edited_by_id` | string |  |
| `filename` | string |  |
| `filesize` | number |  |
| `sha` | string |  |
| `site_id` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `GET /sites/:site_id/collections/:path/files` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collection-files.md) for the provider-specific parameters and requirements.

