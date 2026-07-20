# PassKit Coupons: Update Coupon External Id



```
PUT https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-external-id', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `couponCampaignId` | string | no | Coupon campaign ID when identifying by external ID. |
| `externalId` | string | no | Existing external ID to replace. |
| `id` | string | no | PassKit coupon ID to update. |
| `newExternalId` | string | no | Replacement external ID for the coupon. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `PUT /coupon/singleUse/coupon/externalId` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon-external-id.md) for the provider-specific parameters and requirements.

