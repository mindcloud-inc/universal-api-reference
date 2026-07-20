# Voucherify: List Voucher Redemptions

Retrieves a voucher's redemptions from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-voucher-redemptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-voucher-redemptions?connectionId=$CONNECTION_ID&voucherId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voucherId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-voucher-redemptions?${params}`, {
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
| `voucherId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataRef": "string",
      "object": "string",
      "quantity": 1,
      "redeemedQuantity": 1,
      "redemptionEntries": [
        {}
      ],
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataRef` | string |  |
| `object` | string |  |
| `quantity` | number |  |
| `redeemedQuantity` | number |  |
| `redemptionEntries` | array<object> |  |
| `total` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /vouchers/:voucherId/redemptions` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voucher-redemptions.md) for the provider-specific parameters and requirements.

