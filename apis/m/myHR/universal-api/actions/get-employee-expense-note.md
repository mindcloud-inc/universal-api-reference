# MyHR: Get Employee Expense Note



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-expense-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-expense-note?connectionId=$CONNECTION_ID&employeeExpenseNotePid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeExpenseNotePid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-expense-note?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "creationDate": "string",
      "currency": "string",
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "employee": {
        "isPartial": true,
        "object": "string",
        "pid": "string"
      },
      "employeeExpenseNoteExpenses": [
        {
          "amount": "string",
          "creationDate": "string",
          "dateCreation": "string",
          "dateLastAction": "string",
          "object": "string",
          "pid": "string"
        }
      ],
      "employeeExpenseNoteStatus": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "object": "string",
        "pid": "string",
        "tag": "string"
      },
      "number": "string",
      "object": "string",
      "pid": "string",
      "status": "string",
      "year": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `creationDate` | string |  |
| `currency` | string |  |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `employee.isPartial` | boolean |  |
| `employee.object` | string |  |
| `employee.pid` | string |  |
| `employeeExpenseNoteExpenses[].amount` | string |  |
| `employeeExpenseNoteExpenses[].creationDate` | string |  |
| `employeeExpenseNoteExpenses[].dateCreation` | string |  |
| `employeeExpenseNoteExpenses[].dateLastAction` | string |  |
| `employeeExpenseNoteExpenses[].object` | string |  |
| `employeeExpenseNoteExpenses[].pid` | string |  |
| `employeeExpenseNoteStatus.dateCreation` | string |  |
| `employeeExpenseNoteStatus.dateLastAction` | string |  |
| `employeeExpenseNoteStatus.object` | string |  |
| `employeeExpenseNoteStatus.pid` | string |  |
| `employeeExpenseNoteStatus.tag` | string |  |
| `number` | string |  |
| `object` | string |  |
| `pid` | string |  |
| `status` | string |  |
| `year` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employee_expense_notes/:employee_expense_note_pid` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-expense-note.md) for the provider-specific parameters and requirements.

