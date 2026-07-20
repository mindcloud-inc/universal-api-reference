# Expensify: Create Expenses

Creates new expenses in Expensify.

```
POST https://connect.mindcloud.co/v1/universal/expensify/latest/actions/create-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/create-expenses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeEmail": "ava@example.com",
  "transactionListJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/create-expenses', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeEmail": "ava@example.com",
    "transactionListJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeEmail` | string | yes | The account that should receive the created expenses. |
| `transactionListJson` | string | yes | JSON array of expense objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "category": "string",
      "comment": "string",
      "created": "string",
      "currency": "string",
      "mcc": 1,
      "merchant": "string",
      "reportID": "string",
      "tag": "string",
      "transactionID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `category` | string |  |
| `comment` | string |  |
| `created` | string |  |
| `currency` | string |  |
| `mcc` | number |  |
| `merchant` | string |  |
| `reportID` | string |  |
| `tag` | string |  |
| `transactionID` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expenses.md) for the provider-specific parameters and requirements.

