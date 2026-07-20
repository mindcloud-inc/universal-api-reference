# Intradesk: Evaluate Task

Submits an evaluation for a task in Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/evaluate-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/evaluate-task?connectionId=$CONNECTION_ID&body=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "body": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/evaluate-task?${params}`, {
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
| `body` | object | yes | TaskEvaluationRequestModel JSON object request body documented by Intradesk Changes API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": 1,
      "correlationId": "string",
      "data": {},
      "errorMessage": "string",
      "errorType": 1,
      "id": 1,
      "isSuccess": true,
      "message": "string",
      "messages": {},
      "number": 1,
      "taskProcessType": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | number |  |
| `correlationId` | string |  |
| `data` | object |  |
| `errorMessage` | string |  |
| `errorType` | number |  |
| `id` | number |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `messages` | object |  |
| `number` | number |  |
| `taskProcessType` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `POST /changes/v3/Tasks/evaluate` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/evaluate-task.md) for the provider-specific parameters and requirements.

