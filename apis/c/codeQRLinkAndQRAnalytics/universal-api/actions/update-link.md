# CodeQR - Link and QR Analytics: Update Link

Updates a link in CodeQR.

```
PUT https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "linkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "linkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkId` | string | yes | The ID of the link to update. |
| `title` | string | no | The title of the short link. |

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
      "title": "string",
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
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `PUT /links/:linkId` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

