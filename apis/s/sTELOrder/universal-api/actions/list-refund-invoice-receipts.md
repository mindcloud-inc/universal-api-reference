# STEL Order: List Refund Invoice Receipts

Retrieves a list of refund invoice receipts from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-refund-invoice-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-refund-invoice-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-refund-invoice-receipts?${params}`, {
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
      "account-id": 1,
      "account-path": "string",
      "amount": 1,
      "bank-account-id": 1,
      "bank-account-path": "string",
      "creator-id": 1,
      "creator-path": "string",
      "currency-code": "string",
      "currency-rate": 1,
      "deleted": true,
      "full-reference": "string",
      "id": 1,
      "original-element-id": "string",
      "original-element-path": "string",
      "paid": true,
      "paid-employee-id": 1,
      "paid-employee-path": "string",
      "path": "string",
      "payment-date": "string",
      "payment-option-id": 1,
      "payment-option-path": "string",
      "payment-term-date": "string",
      "settled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account-id` | number |  |
| `account-path` | string |  |
| `amount` | number |  |
| `bank-account-id` | number |  |
| `bank-account-path` | string |  |
| `creator-id` | number |  |
| `creator-path` | string |  |
| `currency-code` | string |  |
| `currency-rate` | number |  |
| `deleted` | boolean |  |
| `full-reference` | string |  |
| `id` | number |  |
| `original-element-id` | string |  |
| `original-element-path` | string |  |
| `paid` | boolean |  |
| `paid-employee-id` | number |  |
| `paid-employee-path` | string |  |
| `path` | string |  |
| `payment-date` | string |  |
| `payment-option-id` | number |  |
| `payment-option-path` | string |  |
| `payment-term-date` | string |  |
| `settled` | boolean |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /refundInvoiceReceipts` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-refund-invoice-receipts.md) for the provider-specific parameters and requirements.

