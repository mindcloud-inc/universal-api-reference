# PassKit Coupons: List Coupon Offers



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupon-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupon-offers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupon-offers?${params}`, {
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
| `campaignId` | string | no | Campaign ID to scope the offer list. |
| `filters.limit` | number | no | Maximum number of offers to return. Default: `25`. |
| `filters.offset` | number | no | Number of offer records to skip. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string"
      },
      "result": {
        "afterRedeemPassTemplateId": "string",
        "beforeRedeemPassTemplateId": "string",
        "campaignId": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "disabled": true,
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `result.afterRedeemPassTemplateId` | string |  |
| `result.beforeRedeemPassTemplateId` | string |  |
| `result.campaignId` | string |  |
| `result.created` | date |  |
| `result.disabled` | boolean |  |
| `result.id` | string |  |
| `result.issueEndDate` | date |  |
| `result.issueStartDate` | date |  |
| `result.offerDetails` | string |  |
| `result.offerFinePrint` | string |  |
| `result.offerShortTitle` | string |  |
| `result.offerTitle` | string |  |
| `result.shortCode` | string |  |
| `result.updated` | date |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `POST /coupon/singleUse/offers/list` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coupon-offers.md) for the provider-specific parameters and requirements.

