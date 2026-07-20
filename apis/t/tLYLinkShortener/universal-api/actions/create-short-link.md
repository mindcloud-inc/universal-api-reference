# TLY Link Shortener: Create Short Link

Creates a new short link in TLY Link Shortener.

```
POST https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "longUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "longUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `longUrl` | string | yes | The destination URL to shorten. |
| `shortId` | string | no | Optional custom short code. |
| `domain` | string | no | Optional branded domain to use for the short link. |
| `description` | string | no | Optional description for the short link. |
| `publicStats` | boolean | no | Whether the short link stats should be public. |
| `expireAtDatetime` | string | no | UTC datetime when the link should expire. |
| `expireAtViews` | number | no | Maximum number of views before the link expires. |
| `password` | string | no | Optional password protecting the short link. |
| `tags[]` | array<number> | no | Optional tag IDs to associate with the short link. |
| `pixels[]` | array<number> | no | Optional pixel IDs to associate with the short link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "expire_at_datetime": "2026-05-07T12:00:00.000Z",
      "expire_at_views": 1,
      "long_url": "https://example.com",
      "meta": {},
      "public_stats": true,
      "short_id": "string",
      "short_url": "https://example.com",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `domain` | string |  |
| `expire_at_datetime` | date |  |
| `expire_at_views` | number |  |
| `long_url` | string |  |
| `meta` | object |  |
| `public_stats` | boolean |  |
| `short_id` | string |  |
| `short_url` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `POST /api/v1/link/shorten` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-short-link.md) for the provider-specific parameters and requirements.

