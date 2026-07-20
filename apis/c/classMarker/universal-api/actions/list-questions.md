# ClassMarker: List Questions



```
GET https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-questions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-questions?${params}`, {
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
      "questions": [
        {
          "categoryId": 1,
          "correctFeedback": "string",
          "incorrectFeedback": "string",
          "lastUpdatedTimestamp": 1,
          "points": "string",
          "question": "string",
          "questionId": 1,
          "questionType": "string",
          "randomAnswers": true,
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `questions[].categoryId` | number |  |
| `questions[].correctFeedback` | string |  |
| `questions[].incorrectFeedback` | string |  |
| `questions[].lastUpdatedTimestamp` | number |  |
| `questions[].points` | string |  |
| `questions[].question` | string |  |
| `questions[].questionId` | number |  |
| `questions[].questionType` | string |  |
| `questions[].randomAnswers` | boolean |  |
| `questions[].status` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `GET /v1/questions.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

