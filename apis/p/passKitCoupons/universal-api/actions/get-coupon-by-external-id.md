# PassKit Coupons: Get Coupon by External ID



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-by-external-id?connectionId=$CONNECTION_ID&couponCampaignId=string&externalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "couponCampaignId": "string",
  "externalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-by-external-id?${params}`, {
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
| `externalId` | string | yes | External ID for the coupon. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "offerId": "string",
      "optOut": true,
      "person": {
        "displayName": "Ava Chen",
        "emailAddress": "ava@example.com",
        "forename": "Ava Chen",
        "surname": "Ava Chen"
      },
      "redemptionDetails": {
        "redemptionCode": "string",
        "redemptionDate": "2026-05-07T12:00:00.000Z"
      },
      "sku": "string",
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |
| `created` | date |  |
| `expiryDate` | date |  |
| `externalId` | string |  |
| `id` | string |  |
| `offerId` | string |  |
| `optOut` | boolean |  |
| `person.displayName` | string |  |
| `person.emailAddress` | string |  |
| `person.forename` | string |  |
| `person.surname` | string |  |
| `redemptionDetails.redemptionCode` | string |  |
| `redemptionDetails.redemptionDate` | date |  |
| `sku` | string |  |
| `status` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `GET /coupon/singleUse/coupon/externalId/:couponCampaignId/:externalId` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon-by-external-id.md) for the provider-specific parameters and requirements.

