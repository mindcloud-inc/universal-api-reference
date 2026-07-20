# Splitwise: Create Expense

Creates a new expense in Splitwise.

```
POST https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cost": "string",
  "description": "string",
  "groupId": 1,
  "splitEqually": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cost": "string",
    "description": "string",
    "groupId": 1,
    "splitEqually": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | number | no | Splitwise category ID for the expense. |
| `cost` | string | yes | Decimal amount as a string with up to 2 decimal places. |
| `currencyCode` | string | no | Splitwise currency code for the expense. |
| `date` | date | no | When the expense took place. |
| `description` | string | yes | Short description of the expense. |
| `details` | string | no | Additional notes for the expense. |
| `groupId` | number | yes | Splitwise group ID to assign the expense to. |
| `repeatInterval` | string | no | Expense recurrence interval. |
| `splitEqually` | boolean | yes | When true, Splitwise will create an equal split within the group. Default: `true`. |

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
| `expenses` | array<object> | Expenses returned by the create call. |

## Native endpoint

Through the native Splitwise API, this operation is `POST /create_expense` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

