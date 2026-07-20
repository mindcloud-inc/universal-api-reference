# Prerender.io: Update Domain 404 Check

Updates a domain 404 check in Prerender.io.

```
PUT https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/put-v3-domain-404-check-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/put-v3-domain-404-check-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enabled": true,
  "id": 1,
  "revisitInterval": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/put-v3-domain-404-check-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enabled": true,
    "id": 1,
    "revisitInterval": 1,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enabled` | boolean | yes |  |
| `id` | number | yes |  |
| `revisitInterval` | number | yes |  |
| `url` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domain": "string",
      "domainCheckSuccess": true,
      "googleIndexedUrlsCount": 1,
      "id": 1,
      "isEnabled": true,
      "lastCheckedAt": "string",
      "randomUrlCheckSuccess": true,
      "revisitInterval": 1,
      "type": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `domain` | string |  |
| `domainCheckSuccess` | boolean |  |
| `googleIndexedUrlsCount` | number |  |
| `id` | number |  |
| `isEnabled` | boolean |  |
| `lastCheckedAt` | string |  |
| `randomUrlCheckSuccess` | boolean |  |
| `revisitInterval` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `PUT /v3/domain-404-check/{id}` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-v3-domain-404-check-id.md) for the provider-specific parameters and requirements.

