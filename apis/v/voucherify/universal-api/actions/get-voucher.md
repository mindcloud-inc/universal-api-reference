# Voucherify: Get Voucher

Retrieves a voucher from Voucherify by code or ID.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-voucher?connectionId=$CONNECTION_ID&voucherId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voucherId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-voucher?${params}`, {
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
      "active": true,
      "category": "string",
      "code": "string",
      "discount": {},
      "id": "string",
      "metadata": {},
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `category` | string |  |
| `code` | string |  |
| `discount` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /vouchers/:voucherId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voucher.md) for the provider-specific parameters and requirements.

