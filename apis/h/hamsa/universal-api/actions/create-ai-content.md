# Hamsa: Create AI Content

Creates AI content in Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-ai-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-ai-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aiParts[]": [
    "string"
  ],
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-ai-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aiParts[]": ["string"],
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aiParts[]` | array<string> | yes | Accepts multiple values as an array. |
| `jobId` | string | yes |  |
| `webhookAuth` | string | no |  |
| `webhookUrl` | string | no |  |

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

Through the native Hamsa API, this operation is `POST /v1/jobs/ai-content` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ai-content.md) for the provider-specific parameters and requirements.

