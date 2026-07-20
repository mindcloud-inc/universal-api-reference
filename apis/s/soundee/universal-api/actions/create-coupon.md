# Soundee: Create Coupon

Creates a new coupon in Soundee.

```
POST https://connect.mindcloud.co/v1/universal/soundee/latest/actions/create-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/soundee/latest/actions/create-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Soundee API, this operation is `POST /coupons` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon.md) for the provider-specific parameters and requirements.

