# Longreads: Get Media

Retrieves a Longreads media item by ID.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-media?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-media?${params}`, {
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
| `id` | number | yes | The media item ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link": "https://example.com",
      "media_type": "string",
      "mime_type": "string",
      "slug": "string",
      "source_url": "https://example.com",
      "title": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number |  |
| `date` | date |  |
| `id` | number |  |
| `link` | string |  |
| `media_type` | string |  |
| `mime_type` | string |  |
| `slug` | string |  |
| `source_url` | string |  |
| `title` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/media/{id}` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media.md) for the provider-specific parameters and requirements.

