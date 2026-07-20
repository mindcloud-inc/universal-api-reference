# Voucherify: Delete Voucher

Deletes an existing voucher from Voucherify.

```
DELETE https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/delete-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/delete-voucher?connectionId=$CONNECTION_ID&voucherId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voucherId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/delete-voucher?${params}`, {
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
      "success": true,
      "voucherId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `voucherId` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `DELETE /vouchers/:voucherId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-voucher.md) for the provider-specific parameters and requirements.

