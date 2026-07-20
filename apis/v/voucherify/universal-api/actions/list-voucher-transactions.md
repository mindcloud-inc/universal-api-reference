# Voucherify: List Voucher Transactions

Retrieves a voucher's transactions from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-voucher-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-voucher-transactions?connectionId=$CONNECTION_ID&voucherId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voucherId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-voucher-transactions?${params}`, {
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
| `voucherId` | string | yes | Voucherify voucher identifier or code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "dataRef": "string",
      "object": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `dataRef` | string |  |
| `object` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /vouchers/:voucherId/transactions` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voucher-transactions.md) for the provider-specific parameters and requirements.

