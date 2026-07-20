# MetaSurvey: Update Question Choice



```
PUT https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/update-question-choice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/update-question-choice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "questionId": "string",
  "choiceId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/update-question-choice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "questionId": "string",
    "choiceId": "string",
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
| `questionId` | string | yes | Question that owns the choice. |
| `choiceId` | string | yes | Choice to update. |
| `text` | string | yes | Updated choice text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "position": 1,
      "question_id": "string",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | MetaSurvey choice identifier. |
| `createdAt` | date | When the choice was created. |
| `position` | number | Choice position within the question. |
| `question_id` | string | Question that owns the choice. |
| `text` | string | Choice text. |
| `updatedAt` | date | When the choice was last updated. |

## Native endpoint

Through the native MetaSurvey API, this operation is `PATCH /admin/survey/:surveyId/question/:questionId/choice/:choiceId` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-question-choice.md) for the provider-specific parameters and requirements.

