# BlockSurvey: Update Survey Text Variable Value

Updates a survey text variable value in BlockSurvey.

```
PUT https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-survey-text-variable-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-survey-text-variable-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "textVariableFlag": true,
  "textVariableName": "Ava Chen",
  "textVariableValue": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-survey-text-variable-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "textVariableFlag": true,
    "textVariableName": "Ava Chen",
    "textVariableValue": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | The ID of the survey. |
| `textVariableFlag` | boolean | yes | Flag to insert, update, or delete the text variable. |
| `textVariableName` | string | yes | The name of the text variable. |
| `textVariableValue` | string | yes | The value of the text variable. |
| `teamId` | string | yes | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `POST /v1/survey/text_variable_value` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-text-variable-value.md) for the provider-specific parameters and requirements.

