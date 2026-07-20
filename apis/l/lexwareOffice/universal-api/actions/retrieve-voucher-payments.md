# Lexware Office: Retrieve Voucher Payments

Retrieves payment information for a voucher in Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-voucher-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-voucher-payments?connectionId=$CONNECTION_ID&voucherId=780a9985-29a1-4daa-aa9c-196ee0dd99f5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voucherId": "780a9985-29a1-4daa-aa9c-196ee0dd99f5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-voucher-payments?${params}`, {
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
| `voucherId` | string | yes | Voucher ID from Lexware. Example: `780a9985-29a1-4daa-aa9c-196ee0dd99f5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "openAmount": 1,
      "paymentItems": [
        {}
      ],
      "paymentStatus": "string",
      "voucherStatus": "string",
      "voucherType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Currency of the voucher payment state. |
| `openAmount` | number | Remaining open amount on the voucher. |
| `paymentItems` | array<object> | Payment items associated with the voucher. |
| `paymentStatus` | string | Payment status classification for the voucher. |
| `voucherStatus` | string | Current voucher status. |
| `voucherType` | string | Voucher type for the payment state. |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/payments/:voucherId` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-voucher-payments.md) for the provider-specific parameters and requirements.

