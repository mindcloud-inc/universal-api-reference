# PassKit Coupons: Update Coupon Offer



```
PUT https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-offer', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "afterRedeemPassTemplateId": "string",
      "beforeRedeemPassTemplateId": "string",
      "campaignId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "ianaTimezone": "string",
      "id": "string",
      "issueEndDate": "2026-05-07T12:00:00.000Z",
      "issueStartDate": "2026-05-07T12:00:00.000Z",
      "offerDetails": "string",
      "offerFinePrint": "string",
      "offerShortTitle": "string",
      "offerTitle": "string",
      "shortCode": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `afterRedeemPassTemplateId` | string |  |
| `beforeRedeemPassTemplateId` | string |  |
| `campaignId` | string |  |
| `created` | date |  |
| `disabled` | boolean |  |
| `ianaTimezone` | string |  |
| `id` | string |  |
| `issueEndDate` | date |  |
| `issueStartDate` | date |  |
| `offerDetails` | string |  |
| `offerFinePrint` | string |  |
| `offerShortTitle` | string |  |
| `offerTitle` | string |  |
| `shortCode` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `PUT /coupon/singleUse/offer` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon-offer.md) for the provider-specific parameters and requirements.

