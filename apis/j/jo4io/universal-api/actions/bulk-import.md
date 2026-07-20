# jo4.io: Bulk Import URLs



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/bulk-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/bulk-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/bulk-import', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string",
      "response": {
        "failureCount": 1,
        "results": [
          {
            "createdUrl": {
              "abTestEnabled": true,
              "abTestMinVisitors": 1,
              "active": true,
              "apiKeyId": 1,
              "contentRating": "https://example.com",
              "conversionTrackingEnabled": true,
              "createdTime": 1,
              "deepLinkEnabled": true,
              "enableIndexing": true,
              "enablePublicStats": true,
              "enableQrPage": true,
              "expired": true,
              "fullShortUrl": "https://example.com",
              "id": 1,
              "longUrl": "https://example.com",
              "malicious": true,
              "modifiedTime": 1,
              "notYetActive": true,
              "nsfw": true,
              "ogType": "https://example.com",
              "passwordProtected": true,
              "previewBeforeRedirect": true,
              "redirectType": "https://example.com",
              "safetyStatus": "https://example.com",
              "shortUrl": "https://example.com",
              "slug": "https://example.com",
              "smartBannerEnabled": true,
              "title": "https://example.com",
              "twitterCard": "https://example.com",
              "userId": 1
            },
            "longUrl": "https://example.com",
            "row": 1,
            "shortUrl": "https://example.com",
            "success": true
          }
        ],
        "successCount": 1,
        "totalProcessed": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string |  |
| `response.failureCount` | number |  |
| `response.results[].createdUrl.abTestEnabled` | boolean |  |
| `response.results[].createdUrl.abTestMinVisitors` | number |  |
| `response.results[].createdUrl.active` | boolean |  |
| `response.results[].createdUrl.apiKeyId` | number |  |
| `response.results[].createdUrl.contentRating` | string |  |
| `response.results[].createdUrl.conversionTrackingEnabled` | boolean |  |
| `response.results[].createdUrl.createdTime` | number |  |
| `response.results[].createdUrl.deepLinkEnabled` | boolean |  |
| `response.results[].createdUrl.enableIndexing` | boolean |  |
| `response.results[].createdUrl.enablePublicStats` | boolean |  |
| `response.results[].createdUrl.enableQrPage` | boolean |  |
| `response.results[].createdUrl.expired` | boolean |  |
| `response.results[].createdUrl.fullShortUrl` | string |  |
| `response.results[].createdUrl.id` | number |  |
| `response.results[].createdUrl.longUrl` | string |  |
| `response.results[].createdUrl.malicious` | boolean |  |
| `response.results[].createdUrl.modifiedTime` | number |  |
| `response.results[].createdUrl.notYetActive` | boolean |  |
| `response.results[].createdUrl.nsfw` | boolean |  |
| `response.results[].createdUrl.ogType` | string |  |
| `response.results[].createdUrl.passwordProtected` | boolean |  |
| `response.results[].createdUrl.previewBeforeRedirect` | boolean |  |
| `response.results[].createdUrl.redirectType` | string |  |
| `response.results[].createdUrl.safetyStatus` | string |  |
| `response.results[].createdUrl.shortUrl` | string |  |
| `response.results[].createdUrl.slug` | string |  |
| `response.results[].createdUrl.smartBannerEnabled` | boolean |  |
| `response.results[].createdUrl.title` | string |  |
| `response.results[].createdUrl.twitterCard` | string |  |
| `response.results[].createdUrl.userId` | number |  |
| `response.results[].longUrl` | string |  |
| `response.results[].row` | number |  |
| `response.results[].shortUrl` | string |  |
| `response.results[].success` | boolean |  |
| `response.successCount` | number |  |
| `response.totalProcessed` | number |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/url/bulk-import` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-import.md) for the provider-specific parameters and requirements.

