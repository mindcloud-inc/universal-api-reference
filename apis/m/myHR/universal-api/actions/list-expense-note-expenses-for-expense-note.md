# MyHR: List Expense Note Expenses For Expense Note



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-expense-note-expenses-for-expense-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-expense-note-expenses-for-expense-note?connectionId=$CONNECTION_ID&employeeExpenseNotePid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeExpenseNotePid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-expense-note-expenses-for-expense-note?${params}`, {
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
| `employeeExpenseNotePid` | string | yes | The employee expense note PID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MyHR API returns.

## Native endpoint

Through the native MyHR API, this operation is `GET /employee_expense_notes/:employee_expense_note_pid/employee_expense_note_expenses` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expense-note-expenses-for-expense-note.md) for the provider-specific parameters and requirements.

