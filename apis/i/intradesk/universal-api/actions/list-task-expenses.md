# Intradesk: List Task Expenses

Retrieves task expenses from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-expenses?connectionId=$CONNECTION_ID&taskNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-expenses?${params}`, {
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
| `taskNumber` | string | yes | Task number from Intradesk TaskForm API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isArchived": true,
      "minutes": 1,
      "taskExpenseLog": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `date` | date |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `minutes` | number |  |
| `taskExpenseLog` | array<object> |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /taskform/api/v2/TaskExpense/{taskNumber}` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-expenses.md) for the provider-specific parameters and requirements.

