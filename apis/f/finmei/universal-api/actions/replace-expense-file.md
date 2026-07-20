# Finmei: Replace Expense File



```
PUT https://connect.mindcloud.co/v1/universal/finmei/latest/actions/replace-expense-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/replace-expense-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "expenseId": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmei/latest/actions/replace-expense-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "expenseId": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expenseId` | string | yes |  |
| `file` | file | yes | Expense file upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": 1,
        "currency": "string",
        "date": "string",
        "id": "string",
        "seller": "string",
        "total": 1,
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | number |  |
| `data.currency` | string |  |
| `data.date` | string |  |
| `data.id` | string |  |
| `data.seller` | string |  |
| `data.total` | number |  |
| `data.updatedAt` | number |  |

## Native endpoint

Through the native Finmei API, this operation is `POST /expenses/:expenseId/file` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-expense-file.md) for the provider-specific parameters and requirements.

