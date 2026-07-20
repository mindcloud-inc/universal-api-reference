# Siteleaf: Get Page

Retrieves a page from Siteleaf.

```
GET https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/get-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/get-page?${params}`, {
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
| `pageId` | string | no | Siteleaf page identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "basename": "Ava Chen",
      "body": "string",
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
| `title` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `GET /pages/:page_id` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

