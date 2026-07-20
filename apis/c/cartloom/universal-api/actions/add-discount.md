# Cartloom: Add Discount

Creates a new discount in Cartloom.

```
POST https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/add-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cartloom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/add-discount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enabled": "1",
  "auto": "0",
  "type": "fixed",
  "unlimited": "0",
  "amount": 1,
  "target": "all",
  "startDate": "2026-05-07T12:00:00.000Z",
  "stopDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/add-discount', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enabled": "1",
    "auto": "0",
    "type": "fixed",
    "unlimited": "0",
    "amount": 1,
    "target": "all",
    "startDate": "2026-05-07T12:00:00.000Z",
    "stopDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enabled` | list | yes | Whether the discount is enabled. Use 1 for enabled or 0 for disabled. One of: `0`, `1`. Default: `1`. |
| `auto` | list | yes | Whether the discount applies automatically. Use 1 or 0. One of: `0`, `1`. Default: `0`. |
| `type` | list | yes | Discount type: fixed or percent. One of: `0`, `1`. Default: `fixed`. |
| `unlimited` | list | yes | Whether redemption is unlimited. Use 1 or 0. One of: `0`, `1`. Default: `0`. |
| `amount` | number | yes | Discount amount as a fixed amount or percentage. |
| `target` | list | yes | Discount target: product, total, or all. One of: `0`, `1`, `2`. Default: `all`. |
| `startDate` | date | yes | Start date in YYYY-MM-DD format. |
| `stopDate` | date | yes | Stop date in YYYY-MM-DD format. |
| `code` | string | no | Code customers enter to get the discount. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetProductIds` | string | no | Target product ID or IDs for product-targeted discounts. |
| `targetAmount` | number | no | Amount required to trigger the discount. |
| `targetQuantity` | number | no | Quantity required to trigger the discount. |
| `allowance` | number | no | Maximum number of times the discount can be redeemed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Newly created discount ID. |
| `result` | string | Cartloom operation result. |

## Native endpoint

Through the native Cartloom API, this operation is `POST /discounts/add/format/json` (base URL `https://mindcloudstage0424.cartloom.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-discount.md) for the provider-specific parameters and requirements.

