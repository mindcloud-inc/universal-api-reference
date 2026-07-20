# MerrenIO: Configure Single Choice Nominal Question



```
PUT https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/configure-single-choice-nominal-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/configure-single-choice-nominal-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "680000000000000000000000",
  "questionId": "690000000000000000000000",
  "questionText": "How satisfied are you?",
  "optionsPayload": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/configure-single-choice-nominal-question', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "680000000000000000000000",
    "questionId": "690000000000000000000000",
    "questionText": "How satisfied are you?",
    "optionsPayload": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey containing the question to configure. Example: `680000000000000000000000`. |
| `questionId` | string | yes | Question to update. Example: `690000000000000000000000`. |
| `questionText` | string | yes | Prompt shown to respondents. Example: `How satisfied are you?`. |
| `optionsPayload` | string | yes | Option list for the nominal question. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /question/updateQuestion` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-single-choice-nominal-question.md) for the provider-specific parameters and requirements.

