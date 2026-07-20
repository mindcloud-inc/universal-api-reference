# DocsBot AI: Get Bot Statistics

Retrieves bot statistics from DocsBot AI.

```
GET https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/get-bot-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/get-bot-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/get-bot-statistics?${params}`, {
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
      "answerCounts": [
        1
      ],
      "answerLabels": [
        "string"
      ],
      "conversationAnsweredCounts": [
        1
      ],
      "conversationAnsweredLabels": [
        "string"
      ],
      "conversationData": [
        1
      ],
      "conversationEscalatedCounts": [
        1
      ],
      "conversationEscalatedLabels": [
        "string"
      ],
      "conversationTopicCounts": [
        1
      ],
      "conversationTopicData": {},
      "conversationTopicLabels": [
        "string"
      ],
      "conversationTopicPieLabels": [
        "string"
      ],
      "couldAnswerData": [
        1
      ],
      "couldAnswerRate": "string",
      "countData": [
        1
      ],
      "counts": [
        1
      ],
      "deflectionRate": "string",
      "escalatedCounts": [
        1
      ],
      "escalatedData": [
        1
      ],
      "escalatedLabels": [
        "string"
      ],
      "labels": [
        "string"
      ],
      "messagesData": [
        1
      ],
      "negativeData": [
        1
      ],
      "percentageLabels": [
        "string"
      ],
      "positiveData": [
        1
      ],
      "resolutionRate": "string",
      "resolvedCounts": [
        1
      ],
      "resolvedLabels": [
        "string"
      ],
      "sentimentCounts": [
        1
      ],
      "sentimentLabels": [
        "string"
      ],
      "timeSaved": 1,
      "totalConversations": 1,
      "totalCount": 1,
      "totalMessages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerCounts` | array<number> |  |
| `answerLabels` | array<string> |  |
| `conversationAnsweredCounts` | array<number> |  |
| `conversationAnsweredLabels` | array<string> |  |
| `conversationData` | array<number> |  |
| `conversationEscalatedCounts` | array<number> |  |
| `conversationEscalatedLabels` | array<string> |  |
| `conversationTopicCounts` | array<number> |  |
| `conversationTopicData` | object |  |
| `conversationTopicLabels` | array<string> |  |
| `conversationTopicPieLabels` | array<string> |  |
| `couldAnswerData` | array<number> |  |
| `couldAnswerRate` | string |  |
| `countData` | array<number> |  |
| `counts` | array<number> |  |
| `deflectionRate` | string |  |
| `escalatedCounts` | array<number> |  |
| `escalatedData` | array<number> |  |
| `escalatedLabels` | array<string> |  |
| `labels` | array<string> |  |
| `messagesData` | array<number> |  |
| `negativeData` | array<number> |  |
| `percentageLabels` | array<string> |  |
| `positiveData` | array<number> |  |
| `resolutionRate` | string |  |
| `resolvedCounts` | array<number> |  |
| `resolvedLabels` | array<string> |  |
| `sentimentCounts` | array<number> |  |
| `sentimentLabels` | array<string> |  |
| `timeSaved` | number |  |
| `totalConversations` | number |  |
| `totalCount` | number |  |
| `totalMessages` | number |  |

## Native endpoint

Through the native DocsBot AI API, this operation is `GET /teams/:teamId/bots/:botId/stats` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-statistics.md) for the provider-specific parameters and requirements.

