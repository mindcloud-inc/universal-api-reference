# MerrenIO: Carry Forward Selected Answers



```
PUT https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/carry-forward-selected-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/carry-forward-selected-answers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "680000000000000000000000",
  "questionId": "690000000000000000000000",
  "sourceQuestionId": "691000000000000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/carry-forward-selected-answers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "680000000000000000000000",
    "questionId": "690000000000000000000000",
    "sourceQuestionId": "691000000000000000000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | Survey containing the target question. Example: `680000000000000000000000`. |
| `questionId` | string | yes | Question receiving carried-forward answers. Example: `690000000000000000000000`. |
| `sourceQuestionId` | string | yes | Question whose selected answers should be carried forward. Example: `691000000000000000000000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /question/updateQuestion` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/carry-forward-selected-answers.md) for the provider-specific parameters and requirements.

