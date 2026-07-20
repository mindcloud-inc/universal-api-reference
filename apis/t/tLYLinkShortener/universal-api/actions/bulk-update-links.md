# TLY Link Shortener: Bulk Update Links

Updates short links in bulk in TLY Link Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-update-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-update-links" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-update-links', {
  method: 'PUT',
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
| `links[]` | array<string> | yes | List of short URLs to update in bulk. |
| `tags[]` | array<number> | no | Optional replacement tag IDs for the provided links. |
| `pixels[]` | array<number> | no | Optional replacement pixel IDs for the provided links. |

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

Through the native TLY Link Shortener API, this operation is `POST /api/v1/link/bulk/update` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-links.md) for the provider-specific parameters and requirements.

