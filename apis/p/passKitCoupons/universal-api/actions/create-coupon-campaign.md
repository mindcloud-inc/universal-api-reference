# PassKit Coupons: Create Coupon Campaign



```
POST https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/create-coupon-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/create-coupon-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/create-coupon-campaign', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | no | Campaign end date. |
| `name` | string | no | Name of the coupon campaign. |
| `offerId` | string | no | Offer ID associated with the campaign. |
| `startDate` | string | no | Campaign start date. |
| `status` | string | no | Project status flags for the campaign. |

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

Through the native PassKit Coupons API, this operation is `POST /coupon/singleUse/campaign` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon-campaign.md) for the provider-specific parameters and requirements.

