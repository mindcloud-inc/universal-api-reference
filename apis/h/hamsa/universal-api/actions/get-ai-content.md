# Hamsa: Get AI Content

Retrieves AI content from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-ai-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-ai-content?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-ai-content?${params}`, {
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
| `jobId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "billingId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jobResponse": {
        "facebookPost": "string",
        "faq": "string",
        "introduction": "string",
        "keyTopicsWithBullets": "string",
        "keywords": "string",
        "linkedInPost": "https://example.com",
        "summary": "string",
        "threadsByInstagram": "string",
        "titles": "string",
        "transcriptionJobId": "string",
        "twitterThread": "string",
        "webArticleSEOFriendly": "string",
        "youtubeDescription": "string"
      },
      "mediaUrl": "https://example.com",
      "model": "string",
      "processingType": "string",
      "relevantJobId": "string",
      "status": "string",
      "systemModelKey": "string",
      "title": "string",
      "totalCost": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usageTime": "string",
      "userId": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string |  |
| `billingId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `jobResponse.facebookPost` | string |  |
| `jobResponse.faq` | string |  |
| `jobResponse.introduction` | string |  |
| `jobResponse.keyTopicsWithBullets` | string |  |
| `jobResponse.keywords` | string |  |
| `jobResponse.linkedInPost` | string |  |
| `jobResponse.summary` | string |  |
| `jobResponse.threadsByInstagram` | string |  |
| `jobResponse.titles` | string |  |
| `jobResponse.transcriptionJobId` | string |  |
| `jobResponse.twitterThread` | string |  |
| `jobResponse.webArticleSEOFriendly` | string |  |
| `jobResponse.youtubeDescription` | string |  |
| `mediaUrl` | string |  |
| `model` | string |  |
| `processingType` | string |  |
| `relevantJobId` | string |  |
| `status` | string |  |
| `systemModelKey` | string |  |
| `title` | string |  |
| `totalCost` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `usageTime` | string |  |
| `userId` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/jobs/ai-content` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-content.md) for the provider-specific parameters and requirements.

