# Soundee: Get Coupon

Retrieves a coupon code from Soundee.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-coupon?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-coupon?${params}`, {
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
| `id` | number | yes | The ID of the coupon. |

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

Through the native Soundee API, this operation is `GET /coupons/:id` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon.md) for the provider-specific parameters and requirements.

