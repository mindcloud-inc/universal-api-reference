# Intradesk: Log Task Expense

Logs a task expense in Intradesk.

```
POST https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/log-task-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/log-task-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/log-task-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | TaskExpensesRequestModel JSON object request body documented by Intradesk Changes API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "correlationId": "string",
      "data": {},
      "errorMessage": "string",
      "errorType": 1,
      "expenses": [
        {}
      ],
      "id": 1,
      "isSuccess": true,
      "message": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `correlationId` | string |  |
| `data` | object |  |
| `errorMessage` | string |  |
| `errorType` | number |  |
| `expenses` | array<object> |  |
| `id` | number |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `PUT /changes/v1/TaskExpenses` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-task-expense.md) for the provider-specific parameters and requirements.

