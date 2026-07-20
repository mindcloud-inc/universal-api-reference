# Bluebarry: Get Answer

Retrieves a single answer from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-answer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-answer?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Bluebarry API, this operation is `GET /data/Answers({id})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-answer.md) for the provider-specific parameters and requirements.

