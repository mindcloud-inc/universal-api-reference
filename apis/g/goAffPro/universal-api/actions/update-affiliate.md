# GoAffPro: Update Affiliate

Updates an existing affiliate in GoAffPro.

```
PUT https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-affiliate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-affiliate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-affiliate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Affiliate ID. |
| `name` | string | no | Affiliate display name. |
| `refCode` | string | no | Referral code for the affiliate. |
| `status` | string | no | Affiliate approval status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commission": {
        "amount": 1,
        "on": "string",
        "type": "string"
      },
      "coupon": {
        "code": "string",
        "discountType": "string",
        "discountValue": 1
      },
      "firstName": "Ava",
      "lastName": "Chen",
      "name": "Ava Chen",
      "refCode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commission.amount` | number |  |
| `commission.on` | string |  |
| `commission.type` | string |  |
| `coupon.code` | string |  |
| `coupon.discountType` | string |  |
| `coupon.discountValue` | number |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `refCode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GoAffPro API, this operation is `PATCH /admin/affiliates/:id` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-affiliate.md) for the provider-specific parameters and requirements.

