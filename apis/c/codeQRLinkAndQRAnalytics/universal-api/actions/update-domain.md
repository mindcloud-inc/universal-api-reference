# CodeQR - Link and QR Analytics: Update Domain

Updates a domain in CodeQR.

```
PUT https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/update-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/update-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/update-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | The domain name. |
| `placeholder` | string | no | Example link placeholder shown in the link creation modal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiredUrl": "https://example.com",
      "id": "string",
      "placeholder": "string",
      "primary": true,
      "slug": "string",
      "target": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `expiredUrl` | string |  |
| `id` | string |  |
| `placeholder` | string |  |
| `primary` | boolean |  |
| `slug` | string |  |
| `target` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `verified` | boolean |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `PATCH /domains/:slug` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain.md) for the provider-specific parameters and requirements.

