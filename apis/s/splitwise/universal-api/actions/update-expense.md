# Splitwise: Update Expense

Updates an existing expense in Splitwise.

```
PUT https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/update-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/update-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/update-expense', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | number | no | Updated Splitwise category ID for the expense. |
| `cost` | string | no | Updated decimal amount as a string with up to 2 decimal places. |
| `currencyCode` | string | no | Updated Splitwise currency code for the expense. |
| `date` | date | no | Updated timestamp for when the expense took place. |
| `description` | string | no | Updated short description of the expense. |
| `details` | string | no | Updated additional notes for the expense. |
| `groupId` | number | no | Updated Splitwise group ID for the expense. |
| `id` | number | yes | Splitwise expense ID to update. |
| `repeatInterval` | string | no | Updated expense recurrence interval. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {},
      "expenses": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | object | Provider-side validation errors when present. |
| `expenses` | array<object> | Expenses returned by the update call. |

## Native endpoint

Through the native Splitwise API, this operation is `POST /update_expense/[:id]` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-expense.md) for the provider-specific parameters and requirements.

