# Porsline: Create Question



```
POST https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "survey_id": 1,
  "title": "string",
  "type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/create-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "survey_id": 1,
    "title": "string",
    "type": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `survey_id` | number | yes | The id of the target survey. |
| `title` | string | yes | Question title. |
| `type` | number | yes | Question type. Use 2 for TextQuestion. |
| `prior_question` | number | no | Prior question id to place the new question after that question. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerRequired": true,
      "answerType": 1,
      "descriptionText": "string",
      "id": 1,
      "imagePath": "string",
      "survey": 1,
      "title": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerRequired` | boolean | Whether an answer is required. |
| `answerType` | number | Answer input type. |
| `descriptionText` | string | Question description text when present. |
| `id` | number | Question ID. |
| `imagePath` | string | Question image path when present. |
| `survey` | number | Owning survey ID. |
| `title` | string | Question title. |
| `type` | number | Porsline question type. |

## Native endpoint

Through the native Porsline API, this operation is `POST /api/v2/surveys/:survey_id/questions/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-question.md) for the provider-specific parameters and requirements.

