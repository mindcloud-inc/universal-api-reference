# Prerender.io: Get Sitemap

Retrieves a sitemap entry from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-sitemap-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-sitemap-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-sitemap-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaptiveType": "string",
      "crawls": [
        {}
      ],
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
| `crawls` | array<object> |  |
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

Through the native Prerender.io API, this operation is `GET /v3/sitemap/{id}` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-sitemap-id.md) for the provider-specific parameters and requirements.

