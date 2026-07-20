# jo4.io: List My URLs



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-urls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-urls?${params}`, {
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
| `withStats` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abTestEnabled": true,
      "abTestMinVisitors": 1,
      "active": true,
      "apiKeyId": 1,
      "contentRating": "string",
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
      "passwordProtected": true,
      "previewBeforeRedirect": true,
      "redirectType": "string",
      "safetyStatus": "string",
      "shortUrl": "https://example.com",
      "slug": "string",
      "smartBannerEnabled": true,
      "title": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abTestEnabled` | boolean |  |
| `abTestMinVisitors` | number |  |
| `active` | boolean |  |
| `apiKeyId` | number |  |
| `contentRating` | string |  |
| `conversionTrackingEnabled` | boolean |  |
| `createdTime` | number |  |
| `deepLinkEnabled` | boolean |  |
| `enableIndexing` | boolean |  |
| `enablePublicStats` | boolean |  |
| `enableQrPage` | boolean |  |
| `expired` | boolean |  |
| `fullShortUrl` | string |  |
| `id` | number |  |
| `longUrl` | string |  |
| `malicious` | boolean |  |
| `modifiedTime` | number |  |
| `notYetActive` | boolean |  |
| `nsfw` | boolean |  |
| `passwordProtected` | boolean |  |
| `previewBeforeRedirect` | boolean |  |
| `redirectType` | string |  |
| `safetyStatus` | string |  |
| `shortUrl` | string |  |
| `slug` | string |  |
| `smartBannerEnabled` | boolean |  |
| `title` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native jo4.io API, this operation is `GET /protected/url/myurls` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-my-urls.md) for the provider-specific parameters and requirements.

