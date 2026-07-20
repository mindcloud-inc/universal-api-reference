# ReferralHero: Create Coupons

Creates coupons in ReferralHero.

```
POST https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/create-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/create-coupons" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "couponGroupId": "string",
  "coupons[]": [
    "string"
  ],
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/create-coupons', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "couponGroupId": "string",
    "coupons[]": ["string"],
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `couponGroupId` | string | yes | Coupon group ID. |
| `coupons[]` | array<string> | yes | Coupon codes to add. Accepts multiple values as an array. |
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "code": "string",
      "createdAt": 1,
      "emailId": "ava@example.com",
      "sentAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `code` | string |  |
| `createdAt` | number |  |
| `emailId` | string |  |
| `sentAt` | string |  |

## Native endpoint

Through the native ReferralHero API, this operation is `POST /lists/:uuid/coupons` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupons.md) for the provider-specific parameters and requirements.

