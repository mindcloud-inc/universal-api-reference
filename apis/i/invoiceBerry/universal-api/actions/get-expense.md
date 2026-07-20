# InvoiceBerry: Get Expense



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-expense?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-expense?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "category_id": "string",
      "currency": "string",
      "date_of_expense": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "notes": "string",
      "tax_amount": "string",
      "tax_name": "Ava Chen",
      "tax_percentage": "string",
      "vendor_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `category_id` | string |  |
| `currency` | string |  |
| `date_of_expense` | date |  |
| `id` | string |  |
| `notes` | string |  |
| `tax_amount` | string |  |
| `tax_name` | string |  |
| `tax_percentage` | string |  |
| `vendor_id` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense.md) for the provider-specific parameters and requirements.

