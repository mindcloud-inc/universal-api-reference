# TAYL: List Tales



```
GET https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/list-tales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAYL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/list-tales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/list-tales?${params}`, {
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
| `limit` | number | no | Maximum number of tales to return. |
| `startAfter` | string | no | Pagination cursor or offset to start after. |
| `status` | string | no | Filter tales by processing status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "byline_author": true,
      "byline_date": true,
      "clearbitLogo": "string",
      "createdAt": {},
      "credits": 1,
      "description": "string",
      "detectedLanguage": "string",
      "excerpt": "string",
      "favIcon": "string",
      "id": "string",
      "language": "string",
      "metaLanguage": "string",
      "publishedAt": "string",
      "publisher": "string",
      "shareImage": "string",
      "source": "string",
      "status": "string",
      "storageMetadataAudio": {},
      "storageMetadataHtml": {},
      "storageMetadataSsml": {},
      "stripeSubscriptionUsageItemId": "string",
      "stripeUsageRecordId": "string",
      "submittedUrl": "https://example.com",
      "summaryLength": 1,
      "title": "string",
      "updatedAt": {},
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `byline_author` | boolean |  |
| `byline_date` | boolean |  |
| `clearbitLogo` | string |  |
| `createdAt` | object |  |
| `credits` | number |  |
| `description` | string |  |
| `detectedLanguage` | string |  |
| `excerpt` | string |  |
| `favIcon` | string |  |
| `id` | string |  |
| `language` | string |  |
| `metaLanguage` | string |  |
| `publishedAt` | string |  |
| `publisher` | string |  |
| `shareImage` | string |  |
| `source` | string |  |
| `status` | string |  |
| `storageMetadataAudio` | object |  |
| `storageMetadataHtml` | object |  |
| `storageMetadataSsml` | object |  |
| `stripeSubscriptionUsageItemId` | string |  |
| `stripeUsageRecordId` | string |  |
| `submittedUrl` | string |  |
| `summaryLength` | number |  |
| `title` | string |  |
| `updatedAt` | object |  |
| `url` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native TAYL API, this operation is `GET /tales` (base URL `https://x.tayl.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tales.md) for the provider-specific parameters and requirements.

