# Prerender.io: Create Sitemap

Creates a sitemap entry in Prerender.io.

```
POST https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-sitemap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "isIntegrationFlow": true,
  "recacheAll": true,
  "revisitInterval": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-sitemap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "isIntegrationFlow": true,
    "recacheAll": true,
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
| `adaptiveType` | string | no |  |
| `isIntegrationFlow` | boolean | yes |  |
| `recacheAll` | boolean | yes |  |
| `revisitInterval` | number | yes |  |
| `url` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaptiveType": "string",
      "createdAt": "string",
      "domain": "string",
      "id": 1,
      "isAvailable": true,
      "isEnabled": true,
      "isHealthy": true,
      "lastCheckedAt": "string",
      "lastVisitedAt": "string",
      "revisitInterval": 1,
      "type": "string",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adaptiveType` | string |  |
| `createdAt` | string |  |
| `domain` | string |  |
| `id` | number |  |
| `isAvailable` | boolean |  |
| `isEnabled` | boolean |  |
| `isHealthy` | boolean |  |
| `lastCheckedAt` | string |  |
| `lastVisitedAt` | string |  |
| `revisitInterval` | number |  |
| `type` | string |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `POST /v3/sitemap` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-v3-sitemap.md) for the provider-specific parameters and requirements.

