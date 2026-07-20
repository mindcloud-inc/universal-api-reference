# Soundee: Update Coupon

Updates an existing coupon in Soundee.

```
PUT https://connect.mindcloud.co/v1/universal/soundee/latest/actions/update-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/update-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/soundee/latest/actions/update-coupon', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the coupon to update. |
| `name` | string | no | The name or code of the coupon. |
| `amount` | number | no | The discount amount. |
| `upgrades` | string | no | Whether the coupon applies to upgrades. |
| `active` | boolean | no | Enable or disable the coupon. |
| `maxUsage` | number | no | Maximum total uses for the coupon. |
| `type` | string | no | The discount type. |
| `minCartItems` | number | no | Minimum number of cart items required. |
| `minCartAmount` | number | no | Minimum cart total required. |
| `stopBulkDiscounts` | boolean | no | Stop further bulk discounts when this coupon applies. |
| `startDate` | string | no | When the coupon becomes active. |
| `endDate` | string | no | When the coupon expires. |
| `neverEnd` | boolean | no | Ignore the end date. |
| `conditions` | object | no | Conditions that define which stores, licenses, entity types, or entities the coupon applies to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "amount": 1,
      "amount_off_string": "string",
      "conditions": {},
      "created": 1,
      "endDate": 1,
      "exclusives": 1,
      "id": 1,
      "maxUsage": 1,
      "minCartAmount": 1,
      "minCartItems": 1,
      "name": "Ava Chen",
      "neverEnd": 1,
      "startDate": 1,
      "stopBulkDiscounts": 1,
      "type": "string",
      "upgrades": 1,
      "used": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `amount` | number |  |
| `amount_off_string` | string |  |
| `conditions` | object |  |
| `created` | number |  |
| `endDate` | number |  |
| `exclusives` | number |  |
| `id` | number |  |
| `maxUsage` | number |  |
| `minCartAmount` | number |  |
| `minCartItems` | number |  |
| `name` | string |  |
| `neverEnd` | number |  |
| `startDate` | number |  |
| `stopBulkDiscounts` | number |  |
| `type` | string |  |
| `upgrades` | number |  |
| `used` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native Soundee API, this operation is `PUT /coupons/:id` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon.md) for the provider-specific parameters and requirements.

