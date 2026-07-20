# Prerender.io: Create Sitemap Crawl

Starts a sitemap crawl in Prerender.io.

```
POST https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-sitemap-id-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-sitemap-id-crawl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "recacheAll": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-sitemap-id-crawl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "recacheAll": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adaptiveType` | string | no |  |
| `id` | number | yes |  |
| `recacheAll` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adaptiveType": "string",
      "createdAt": "string",
      "id": 1,
      "result": {},
      "runtime": 1,
      "sitemapId": 1,
      "status": "string",
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
| `adaptiveType` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `result` | object |  |
| `runtime` | number |  |
| `sitemapId` | number |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `POST /v3/sitemap/{id}/crawl` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-v3-sitemap-id-crawl.md) for the provider-specific parameters and requirements.

