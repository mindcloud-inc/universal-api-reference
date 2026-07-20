# TLY Link Shortener: Update Short Link

Updates an existing short link in TLY Link Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-short-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shortUrl` | string | yes | The short URL to update. |
| `shortId` | string | no | Optional replacement short code. |
| `longUrl` | string | no | The updated destination URL. |
| `description` | string | no | Optional updated description for the short link. |
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
      "has_password": true,
      "long_url": "https://example.com",
      "meta": {},
      "pixels": [
        {}
      ],
      "public_stats": true,
      "qr_code": {},
      "short_id": "string",
      "short_url": "https://example.com",
      "tags": [
        {}
      ],
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
| `has_password` | boolean |  |
| `long_url` | string |  |
| `meta` | object |  |
| `pixels` | array<object> |  |
| `public_stats` | boolean |  |
| `qr_code` | object |  |
| `short_id` | string |  |
| `short_url` | string |  |
| `tags` | array<object> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `PUT /api/v1/link` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-short-link.md) for the provider-specific parameters and requirements.

