# MetaSurvey: Duplicate Survey Question



```
POST https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/duplicate-survey-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/duplicate-survey-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "questionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/duplicate-survey-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "questionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey that owns the question. |
| `questionId` | string | yes | Question to duplicate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "choices_count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "position": 1,
      "surveyId": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | MetaSurvey question identifier. |
| `choices_count` | number | Number of choices on the duplicated question. |
| `createdAt` | date | When the duplicated question was created. |
| `position` | number | Question position within the survey. |
| `surveyId` | string | Survey that owns the question. |
| `text` | string | Question text. |
| `type` | string | Question type. |

## Native endpoint

Through the native MetaSurvey API, this operation is `POST /admin/survey/:surveyId/question/:questionId/duplicate` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-survey-question.md) for the provider-specific parameters and requirements.

