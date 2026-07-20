# ClassMarker: Get Question



```
GET https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/get-question?connectionId=$CONNECTION_ID&questionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/get-question?${params}`, {
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
| `questionId` | number | yes | Numeric ClassMarker question ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "correctFeedback": "string",
      "correctOptions": [
        [
          "string"
        ]
      ],
      "gradeStyle": "string",
      "incorrectFeedback": "string",
      "lastUpdatedTimestamp": 1,
      "options": {},
      "points": "string",
      "question": "string",
      "questionId": 1,
      "questionType": "string",
      "randomAnswers": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `correctFeedback` | string |  |
| `correctOptions[]` | array<string> |  |
| `gradeStyle` | string |  |
| `incorrectFeedback` | string |  |
| `lastUpdatedTimestamp` | number |  |
| `options` | object |  |
| `points` | string |  |
| `question` | string |  |
| `questionId` | number |  |
| `questionType` | string |  |
| `randomAnswers` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `GET /v1/questions/{question_id}.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

