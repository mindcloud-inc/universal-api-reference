# CodeQR - Link and QR Analytics: Create Link

Creates a link in CodeQR.

```
POST https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/create-link', {
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
| `url` | string | yes | The destination URL of the short link. |
| `externalId` | string | no | The external ID for the link in your system. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "clicks": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "externalId": "string",
      "id": "string",
      "key": "string",
      "shortLink": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `clicks` | number |  |
| `createdAt` | date |  |
| `domain` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `key` | string |  |
| `shortLink` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `POST /links` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link.md) for the provider-specific parameters and requirements.

