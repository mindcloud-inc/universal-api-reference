# MetaSurvey: Delete Survey Question



```
DELETE https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/delete-survey-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MetaSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/delete-survey-question?connectionId=$CONNECTION_ID&surveyId=string&questionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string",
  "questionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/delete-survey-question?${params}`, {
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
| `surveyId` | string | yes | Survey that owns the question. |
| `questionId` | string | yes | Question to delete. |

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
| `createdAt` | date | When the question was created. |
| `position` | number | Question position within the survey. |
| `surveyId` | string | Survey that owned the question. |
| `text` | string | Question text. |
| `type` | string | Question type. |

## Native endpoint

Through the native MetaSurvey API, this operation is `DELETE /admin/survey/:surveyId/question/:questionId` (base URL `https://api.getmetasurvey.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-survey-question.md) for the provider-specific parameters and requirements.

