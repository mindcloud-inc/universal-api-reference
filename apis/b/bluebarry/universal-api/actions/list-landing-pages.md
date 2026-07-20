# Bluebarry: List Landing Pages

Retrieves landing page records from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-landing-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-landing-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-landing-pages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "clonedFrom": "string",
      "cloudflareCustomHostnameId": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "customDomain": "string",
      "customDomainVerified": true,
      "faviconUrl": "https://example.com",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "name": "Ava Chen",
      "path": "string",
      "reference": "string",
      "sections": [
        {}
      ],
      "seoDescription": "string",
      "seoTitle": "string",
      "status": "string",
      "tenant": "string",
      "tenantId": "string",
      "theme": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clonedFrom` | string |  |
| `cloudflareCustomHostnameId` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `customDomain` | string |  |
| `customDomainVerified` | boolean |  |
| `faviconUrl` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `name` | string |  |
| `path` | string |  |
| `reference` | string |  |
| `sections` | array<object> |  |
| `seoDescription` | string |  |
| `seoTitle` | string |  |
| `status` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `theme` | string |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/LandingPages` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-landing-pages.md) for the provider-specific parameters and requirements.

