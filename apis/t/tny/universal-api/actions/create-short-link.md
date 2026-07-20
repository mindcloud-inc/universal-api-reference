# Tny: Create Short Link

Creates a shortened link in Tny.

```
POST https://connect.mindcloud.co/v1/universal/tny/latest/actions/create-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tny/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tny/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The HTTP or HTTPS URL to shorten. |
| `customSlug` | string | no | Optional custom slug. Requires a custom domain and Developer tier. |
| `domainId` | string | no | Optional custom domain UUID for the short link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customDomain": "string",
      "domainId": "string",
      "longUrl": "https://example.com",
      "qrDownloadUrl": "https://example.com",
      "shortUrl": "https://example.com",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the short link was created. |
| `customDomain` | string | Custom domain used by the short link when present. |
| `domainId` | string | Custom domain identifier when present. |
| `longUrl` | string | Original destination URL. |
| `qrDownloadUrl` | string | QR code download URL for the short link. |
| `shortUrl` | string | Shortened URL. |
| `slug` | string | Generated short-link slug. |

## Native endpoint

Through the native Tny API, this operation is `POST /api/v1/shorten` (base URL `https://www.tny.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-short-link.md) for the provider-specific parameters and requirements.

