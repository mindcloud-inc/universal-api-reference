# BlockSurvey: Get Survey Text Variable Value

Retrieves a survey text variable value from BlockSurvey.

```
GET https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-text-variable-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-text-variable-value?connectionId=$CONNECTION_ID&surveyId=string&textVariableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string",
  "textVariableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-text-variable-value?${params}`, {
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
| `surveyId` | string | yes | The ID of the survey. |
| `textVariableName` | string | yes | The name of the text variable. |
| `teamId` | string | no | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "textVariableValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `textVariableValue` | string |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `GET /v1/survey/text_variable_value` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-text-variable-value.md) for the provider-specific parameters and requirements.

