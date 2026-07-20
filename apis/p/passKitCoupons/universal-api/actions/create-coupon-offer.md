# PassKit Coupons: Create Coupon Offer



```
POST https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/create-coupon-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/create-coupon-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/create-coupon-offer', {
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
| `beforeRedeemPassTemplateId` | string | no | Pass template ID used before redemption. |
| `campaignId` | string | no | Coupon campaign ID for this offer when applicable. |
| `issueEndDate` | string | no | Offer issuance end date in RFC3339 format. |
| `issueStartDate` | string | no | Offer issuance start date in RFC3339 format. |
| `offerDetails` | string | no | Offer details shown on the coupon offer. |
| `offerShortTitle` | string | no | Short title for the coupon offer. |
| `offerTitle` | string | no | Offer title for the coupon offer. |

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

Through the native PassKit Coupons API, this operation is `POST /coupon/singleUse/offer` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon-offer.md) for the provider-specific parameters and requirements.

