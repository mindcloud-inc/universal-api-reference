# STEL Order: List Refund Invoices

Retrieves a list of refund invoices from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-refund-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-refund-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-refund-invoices?${params}`, {
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
      "agent-id": 1,
      "agent-path": "string",
      "assets": [
        "string"
      ],
      "bank-account-id": 1,
      "bank-account-path": "string",
      "creation-date": "string",
      "creator-id": 1,
      "creator-path": "string",
      "currency-code": "string",
      "currency-rate": 1,
      "date": "string",
      "deleted": true,
      "discount-percentage": 1,
      "discount-total-amount": 1,
      "document-state-id": 1,
      "document-state-path": "string",
      "email-read-count": 1,
      "full-reference": "string",
      "id": 1,
      "income-tax-enabled": true,
      "income-tax-percentage": 1,
      "invoicing-address-id": 1,
      "invoicing-address-path": "string",
      "lines": [
        {}
      ],
      "paid-total-amount": 1,
      "path": "string",
      "payment-option-id": 1,
      "payment-option-path": "string",
      "payment-terms-id": 1,
      "payment-terms-path": "string",
      "pdf-path": "string",
      "primary-tax-enabled": true,
      "receipts": [
        {}
      ],
      "reference": "string",
      "remaining-total-amount": 1,
      "secondary-tax-enabled": true,
      "serial-number-id": 1,
      "serial-number-path": "string",
      "settled": true,
      "signed": true,
      "subtotal-amount": 1,
      "tax-breakdown": [
        {}
      ],
      "tax-total-amount": 1,
      "total-amount": 1
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
| `agent-id` | number |  |
| `agent-path` | string |  |
| `assets` | array |  |
| `bank-account-id` | number |  |
| `bank-account-path` | string |  |
| `creation-date` | string |  |
| `creator-id` | number |  |
| `creator-path` | string |  |
| `currency-code` | string |  |
| `currency-rate` | number |  |
| `date` | string |  |
| `deleted` | boolean |  |
| `discount-percentage` | number |  |
| `discount-total-amount` | number |  |
| `document-state-id` | number |  |
| `document-state-path` | string |  |
| `email-read-count` | number |  |
| `full-reference` | string |  |
| `id` | number |  |
| `income-tax-enabled` | boolean |  |
| `income-tax-percentage` | number |  |
| `invoicing-address-id` | number |  |
| `invoicing-address-path` | string |  |
| `lines` | array<object> |  |
| `paid-total-amount` | number |  |
| `path` | string |  |
| `payment-option-id` | number |  |
| `payment-option-path` | string |  |
| `payment-terms-id` | number |  |
| `payment-terms-path` | string |  |
| `pdf-path` | string |  |
| `primary-tax-enabled` | boolean |  |
| `receipts` | array<object> |  |
| `reference` | string |  |
| `remaining-total-amount` | number |  |
| `secondary-tax-enabled` | boolean |  |
| `serial-number-id` | number |  |
| `serial-number-path` | string |  |
| `settled` | boolean |  |
| `signed` | boolean |  |
| `subtotal-amount` | number |  |
| `tax-breakdown` | array<object> |  |
| `tax-total-amount` | number |  |
| `total-amount` | number |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /refundInvoices` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-refund-invoices.md) for the provider-specific parameters and requirements.

