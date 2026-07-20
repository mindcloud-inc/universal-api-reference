# PassKit Coupons: List Coupons



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupons?connectionId=$CONNECTION_ID&couponCampaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "couponCampaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupons?${params}`, {
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
| `couponCampaignId` | string | yes | Coupon campaign ID. |
| `emailAsCsv` | boolean | no | Email the coupon list as a CSV instead of returning it directly. Default: `false`. |
| `filters.limit` | number | no | Maximum number of coupons to return. Default: `25`. |
| `filters.offset` | number | no | Number of coupon records to skip. Default: `0`. |

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
        "campaignId": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "expiryDate": "2026-05-07T12:00:00.000Z",
        "externalId": "string",
        "id": "string",
        "offerId": "string",
        "person": {
          "displayName": "Ava Chen",
          "emailAddress": "ava@example.com"
        },
        "redemptionDetails": {
          "redemptionDate": "2026-05-07T12:00:00.000Z"
        },
        "sku": "string",
        "status": "string",
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
| `result.campaignId` | string |  |
| `result.created` | date |  |
| `result.expiryDate` | date |  |
| `result.externalId` | string |  |
| `result.id` | string |  |
| `result.offerId` | string |  |
| `result.person.displayName` | string |  |
| `result.person.emailAddress` | string |  |
| `result.redemptionDetails.redemptionDate` | date |  |
| `result.sku` | string |  |
| `result.status` | string |  |
| `result.updated` | date |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `POST /coupon/singleUse/coupons/list/:couponCampaignId` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

