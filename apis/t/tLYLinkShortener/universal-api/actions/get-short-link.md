# TLY Link Shortener: Get Short Link

Retrieves a short link from TLY Link Shortener.

```
GET https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-short-link?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-short-link?${params}`, {
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
| `shortUrl` | string | yes | The short URL to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can_edit_disabled": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "expire_at_datetime": "2026-05-07T12:00:00.000Z",
      "expire_at_views": 1,
      "long_url": "https://example.com",
      "meta": {},
      "pixels": [
        {}
      ],
      "public_stats": true,
      "qr_code_base64": "string",
      "qr_code_url": "https://example.com",
      "safe_link": "https://example.com",
      "short_id": "string",
      "short_stats": {},
      "short_url": "https://example.com",
      "tags": [
        {}
      ],
      "team_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user": {},
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_edit_disabled` | boolean |  |
| `created_at` | date |  |
| `description` | string |  |
| `domain` | string |  |
| `expire_at_datetime` | date |  |
| `expire_at_views` | number |  |
| `long_url` | string |  |
| `meta` | object |  |
| `pixels` | array<object> |  |
| `public_stats` | boolean |  |
| `qr_code_base64` | string |  |
| `qr_code_url` | string |  |
| `safe_link` | string |  |
| `short_id` | string |  |
| `short_stats` | object |  |
| `short_url` | string |  |
| `tags` | array<object> |  |
| `team_id` | number |  |
| `updated_at` | date |  |
| `user` | object |  |
| `user_id` | number |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `GET /api/v1/link` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-short-link.md) for the provider-specific parameters and requirements.

