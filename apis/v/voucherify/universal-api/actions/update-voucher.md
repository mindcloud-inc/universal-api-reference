# Voucherify: Update Voucher

Updates an existing voucher in Voucherify.

```
PUT https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/update-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/update-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voucherId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/update-voucher', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voucherId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no |  |
| `voucherId` | string | yes |  |

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

Through the native Voucherify API, this operation is `PUT /vouchers/:voucherId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voucher.md) for the provider-specific parameters and requirements.

