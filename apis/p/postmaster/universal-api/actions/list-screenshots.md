# Postmaster+: List Screenshots

Retrieves screenshots from the Postmaster+ API.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/list-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/list-screenshots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/list-screenshots?${params}`, {
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
| `sort` | string | no | Sort order for screenshots. Supported values: created_at, -created_at, format, -format. One of: `0`, `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "creditsUsed": 1,
      "format": "string",
      "height": 1,
      "id": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `creditsUsed` | number | Credits consumed. |
| `format` | string | Image format. |
| `height` | number | Screenshot height. |
| `id` | string | Screenshot ULID. |
| `url` | string | Screenshot URL. |
| `width` | number | Screenshot width. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/screenshots` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-screenshots.md) for the provider-specific parameters and requirements.

