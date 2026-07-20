# Soundee: List Coupons

Retrieves your coupon codes from Soundee.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-coupons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-coupons?${params}`, {
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
| `listType` | string | no | Filter coupons by state. |
| `search` | string | no | Search coupons by name or amount. |

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

Through the native Soundee API, this operation is `GET /coupons` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

