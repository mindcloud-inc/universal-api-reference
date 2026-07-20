# Hamsa: Create Customized AI Content

Creates customized AI content in Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-customized-ai-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-customized-ai-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aiParts[]": [
    {}
  ],
  "aiParts[].aiPart": "string",
  "aiParts[].language": "string",
  "aiParts[].prompt": "string",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-customized-ai-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aiParts[]": [{}],
    "aiParts[]": [{}],
    "aiParts[].aiPart": "string",
    "aiParts[].aiPart": "string",
    "aiParts[].language": "string",
    "aiParts[].language": "string",
    "aiParts[].prompt": "string",
    "aiParts[].prompt": "string",
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aiParts[]` | array<object> | yes | Accepts multiple values as an array. |
| `aiParts[]` | array<object> | yes |  |
| `aiParts[].aiPart` | string | yes |  |
| `aiParts[].aiPart` | string | yes |  |
| `aiParts[].language` | string | yes |  |
| `aiParts[].language` | string | yes |  |
| `aiParts[].prompt` | string | yes |  |
| `aiParts[].prompt` | string | yes |  |
| `jobId` | string | yes |  |
| `webhookAuth` | object | no |  |
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

Through the native Hamsa API, this operation is `POST /v1/jobs/ai-content/custom` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customized-ai-content.md) for the provider-specific parameters and requirements.

