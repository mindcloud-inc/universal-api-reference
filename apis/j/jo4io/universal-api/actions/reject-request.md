# jo4.io: Reject Transfer Request



```
PUT https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/reject-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/reject-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/reject-request', {
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
| `slug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": 1,
      "expiresAt": 1,
      "id": 1,
      "message": "string",
      "ownerEmail": "ava@example.com",
      "ownerId": 1,
      "requesterEmail": "ava@example.com",
      "requesterId": 1,
      "respondedAt": 1,
      "shortUrl": "https://example.com",
      "slug": "string",
      "status": "string",
      "transferType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number |  |
| `expiresAt` | number |  |
| `id` | number |  |
| `message` | string |  |
| `ownerEmail` | string |  |
| `ownerId` | number |  |
| `requesterEmail` | string |  |
| `requesterId` | number |  |
| `respondedAt` | number |  |
| `shortUrl` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `transferType` | string |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/transfer-request/:slug/reject` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reject-request.md) for the provider-specific parameters and requirements.

