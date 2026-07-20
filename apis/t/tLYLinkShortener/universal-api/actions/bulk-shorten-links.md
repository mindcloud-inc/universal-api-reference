# TLY Link Shortener: Bulk Shorten Links

Creates short links in bulk in TLY Link Shortener.

```
POST https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-shorten-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-shorten-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-shorten-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `links[]` | array<string> | yes | List of destination URLs to shorten in bulk. |
| `domain` | string | no | Optional branded domain to use for every generated short link. |
| `tags[]` | array<number> | no | Optional tag IDs to attach to every generated short link. |
| `pixels[]` | array<number> | no | Optional pixel IDs to attach to every generated short link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | boolean |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `POST /api/v1/link/bulk` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-shorten-links.md) for the provider-specific parameters and requirements.

