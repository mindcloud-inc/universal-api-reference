# InvoiceBerry: Get Client Credit History



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-client-credit-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-client-credit-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/get-client-credit-history?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "payment_id": "string",
      "payment_type_id": "string",
      "payment_type_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `date` | date |  |
| `notes` | string |  |
| `payment_id` | string |  |
| `payment_type_id` | string |  |
| `payment_type_name` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-credit-history.md) for the provider-specific parameters and requirements.

