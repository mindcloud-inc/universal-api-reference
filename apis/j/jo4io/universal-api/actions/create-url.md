# jo4.io: Create URL



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "longUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "longUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customDomain` | string | no |  |
| `longUrl` | string | yes |  |
| `shortUrl` | string | no |  |
| `teamId` | string | no |  |
| `title` | string | no |  |

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

Through the native jo4.io API, this operation is `POST /protected/url` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-url.md) for the provider-specific parameters and requirements.

