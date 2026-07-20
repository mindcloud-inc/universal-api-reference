# Reepay: List Charges

Retrieves charges from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-charges?${params}`, {
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
      "amount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": "string",
      "handle": "string",
      "order_lines": [
        {
          "amount": 1,
          "ordertext": "string",
          "quantity": 1,
          "vat": 1
        }
      ],
      "payment_context": {},
      "processing": true,
      "refunded_amount": 1,
      "source": {
        "offline_agreement_handle": "string",
        "offline_payment_instructions": "string",
        "type": "string"
      },
      "state": "string",
      "transaction": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created` | date |  |
| `currency` | string |  |
| `customer` | string |  |
| `handle` | string |  |
| `order_lines[].amount` | number |  |
| `order_lines[].ordertext` | string |  |
| `order_lines[].quantity` | number |  |
| `order_lines[].vat` | number |  |
| `payment_context` | object |  |
| `processing` | boolean |  |
| `refunded_amount` | number |  |
| `source.offline_agreement_handle` | string |  |
| `source.offline_payment_instructions` | string |  |
| `source.type` | string |  |
| `state` | string |  |
| `transaction` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/list/charge` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-charges.md) for the provider-specific parameters and requirements.

