# QuestionPro Surveys: Get Survey Block



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey-block?connectionId=$CONNECTION_ID&surveyId=13483869&blockId=2927440" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "13483869",
  "blockId": "2927440"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey-block?${params}`, {
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
| `surveyId` | number | yes | The QuestionPro survey ID. Example: `13483869`. |
| `blockId` | number | yes | The QuestionPro survey block ID. Example: `2927440`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockID": 1,
      "creationDate": "string",
      "orderNumber": 1,
      "surveyID": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockID` | number | The QuestionPro survey block ID. |
| `creationDate` | string | The block creation date. |
| `orderNumber` | number | The display order of the block within the survey. |
| `surveyID` | number | The QuestionPro survey ID. |
| `title` | string | The block title. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId/blocks/:blockId` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-block.md) for the provider-specific parameters and requirements.

