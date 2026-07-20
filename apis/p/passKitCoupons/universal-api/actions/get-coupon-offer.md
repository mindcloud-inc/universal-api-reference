# PassKit Coupons: Get Coupon Offer



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-offer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-offer?${params}`, {
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
| `id` | string | yes | Coupon offer ID. |

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

Through the native PassKit Coupons API, this operation is `GET /coupon/singleUse/offer/:id` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon-offer.md) for the provider-specific parameters and requirements.

