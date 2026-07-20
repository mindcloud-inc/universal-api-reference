# PayTabs: Refund Transaction



```
PUT https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/refund-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/refund-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cart_id": "string",
  "cart_currency": "string",
  "cart_amount": 1,
  "cart_description": "string",
  "tran_ref": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/refund-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cart_id": "string",
    "cart_currency": "string",
    "cart_amount": 1,
    "cart_description": "string",
    "tran_ref": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cart_id` | string | yes | Merchant cart or order identifier. |
| `cart_currency` | string | yes | Transaction currency. |
| `cart_amount` | number | yes | Transaction amount to refund. |
| `cart_description` | string | yes | Reason or description for the refund. |
| `tran_ref` | string | yes | Captured or sale PayTabs transaction reference. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cartId": "string",
      "code": 1,
      "message": "string",
      "paymentResult": {},
      "trace": "string",
      "tranRef": "string",
      "tranType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartId` | string |  |
| `code` | number |  |
| `message` | string |  |
| `paymentResult` | object |  |
| `trace` | string |  |
| `tranRef` | string |  |
| `tranType` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/request` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-transaction.md) for the provider-specific parameters and requirements.

