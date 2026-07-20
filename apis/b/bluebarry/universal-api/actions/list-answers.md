# Bluebarry: List Answers

Retrieves answer entity records from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-answers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/list-answers?${params}`, {
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
      "answerFilters": [
        {}
      ],
      "answerFormat": "string",
      "answerSkipsQuestions": [
        {}
      ],
      "answerTexts": [
        {}
      ],
      "answerType": "string",
      "clonedFrom": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "extraInformation": "string",
      "fullAnswerText": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "label": "string",
      "maxValue": 1,
      "minValue": 1,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "order": 1,
      "question": "string",
      "questionId": "string",
      "reference": "string",
      "staticName": "Ava Chen",
      "tenant": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerFilters` | array<object> |  |
| `answerFormat` | string |  |
| `answerSkipsQuestions` | array<object> |  |
| `answerTexts` | array<object> |  |
| `answerType` | string |  |
| `clonedFrom` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `extraInformation` | string |  |
| `fullAnswerText` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `label` | string |  |
| `maxValue` | number |  |
| `minValue` | number |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `order` | number |  |
| `question` | string |  |
| `questionId` | string |  |
| `reference` | string |  |
| `staticName` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/Answers` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-answers.md) for the provider-specific parameters and requirements.

