# Voucherify: Create Voucher

Creates a new voucher in Voucherify.

```
POST https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amountOff": 1,
  "code": "string",
  "discountType": "AMOUNT",
  "voucherType": "DISCOUNT_VOUCHER"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-voucher', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amountOff": 1,
    "code": "string",
    "discountType": "AMOUNT",
    "voucherType": "DISCOUNT_VOUCHER"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amountOff` | number | yes |  |
| `code` | string | yes |  |
| `discountType` | string | yes | Default: `AMOUNT`. |
| `voucherType` | string | yes | Default: `DISCOUNT_VOUCHER`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "campaign": "string",
      "campaignId": "string",
      "categories": [
        "string"
      ],
      "category": "string",
      "categoryId": "string",
      "code": "string",
      "createdAt": "string",
      "discount": {},
      "id": "string",
      "metadata": {},
      "object": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `campaign` | string |  |
| `campaignId` | string |  |
| `categories` | array<string> |  |
| `category` | string |  |
| `categoryId` | string |  |
| `code` | string |  |
| `createdAt` | string |  |
| `discount` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `POST /vouchers` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voucher.md) for the provider-specific parameters and requirements.

