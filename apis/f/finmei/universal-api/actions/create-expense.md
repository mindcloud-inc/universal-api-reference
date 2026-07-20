# Finmei: Create Expense



```
POST https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "file": "string",
  "seller": "string",
  "total": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency": "string",
    "date": "2026-05-07T12:00:00.000Z",
    "file": "string",
    "seller": "string",
    "total": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | yes | Expense currency code. |
| `date` | date | yes | Expense date. |
| `file` | file | yes | Expense file upload. |
| `seller` | string | yes | Expense seller name. |
| `total` | number | yes | Expense total amount. |

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

Through the native Finmei API, this operation is `POST /expenses` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

