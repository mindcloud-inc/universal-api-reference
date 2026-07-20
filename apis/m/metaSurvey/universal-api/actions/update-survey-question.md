# MetaSurvey: Update Survey Question



```
PUT https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/update-survey-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/update-survey-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "questionId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/update-survey-question', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "questionId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey that owns the question. |
| `questionId` | string | yes | Question to update. |
| `text` | string | yes | Updated question text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "position": 1,
      "surveyId": "string",
      "text": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | MetaSurvey question identifier. |
| `createdAt` | date | When the question was created. |
| `position` | number | Question position within the survey. |
| `surveyId` | string | Survey that owns the question. |
| `text` | string | Question text. |
| `type` | string | Question type. |
| `updatedAt` | date | When the question was last updated. |

## Native endpoint

Through the native MetaSurvey API, this operation is `PATCH /admin/survey/:surveyId/question/:questionId` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-question.md) for the provider-specific parameters and requirements.

