# Olostep: Get Crawl

Retrieves details for a crawl in Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-crawl?connectionId=$CONNECTION_ID&crawlId=crawl_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlId": "crawl_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-crawl?${params}`, {
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
| `crawlId` | string | yes | The ID of the crawl to retrieve. Example: `crawl_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "currentDepth": 1,
      "id": "string",
      "includeExternal": true,
      "includeUrls": [
        "https://example.com"
      ],
      "maxDepth": {},
      "maxPages": 1,
      "object": "string",
      "pagesCount": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "startUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `currentDepth` | number |  |
| `id` | string |  |
| `includeExternal` | boolean |  |
| `includeUrls[]` | string |  |
| `maxDepth` | object |  |
| `maxPages` | number |  |
| `object` | string |  |
| `pagesCount` | number |  |
| `startDate` | date |  |
| `startUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/crawls/[:crawl_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl.md) for the provider-specific parameters and requirements.

