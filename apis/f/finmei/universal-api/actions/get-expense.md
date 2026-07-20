# Finmei: Get Expense



```
GET https://connect.mindcloud.co/v1/universal/finmei/latest/actions/get-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/get-expense?connectionId=$CONNECTION_ID&expenseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expenseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmei/latest/actions/get-expense?${params}`, {
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
| `expenseId` | string | yes |  |

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

Through the native Finmei API, this operation is `GET /expenses/:expenseId` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense.md) for the provider-specific parameters and requirements.

