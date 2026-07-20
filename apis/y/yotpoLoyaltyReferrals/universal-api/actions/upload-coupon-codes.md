# Yotpo Loyalty & Referrals: Upload Coupon Codes

Uploads coupon codes to Yotpo Loyalty & Referrals.

```
POST https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/upload-coupon-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/upload-coupon-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "redemptionOptionId": 1,
  "codes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/upload-coupon-codes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "redemptionOptionId": 1,
    "codes": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `redemptionOptionId` | number | yes | Redemption option ID returned by the active redemption options endpoint. |
| `codes` | string | yes | Comma-separated coupon codes to upload. Up to 10,000 codes are allowed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "appliesToProductType": "string",
      "cartGreaterThan": "string",
      "costText": "string",
      "description": "string",
      "discountAmountCents": 1,
      "discountPercentage": 1,
      "discountRateCents": 1,
      "discountType": "string",
      "discountValueCents": 1,
      "discountWithCurrency": "string",
      "duration": "string",
      "icon": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "unrenderedDescription": "string",
      "unrenderedName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Points amount required for the redemption option. |
| `appliesToProductType` | string | Product applicability scope for the coupon. |
| `cartGreaterThan` | string | Minimum cart threshold returned by Yotpo. |
| `costText` | string | Human-readable points cost text. |
| `description` | string | Description of the redemption option. |
| `discountAmountCents` | number | Fixed discount amount in cents. |
| `discountPercentage` | number | Discount percentage for the option. |
| `discountRateCents` | number | Discount rate amount in cents when applicable. |
| `discountType` | string | Discount type returned by Yotpo. |
| `discountValueCents` | number | Discount value in cents. |
| `discountWithCurrency` | string | Currency-formatted discount text. |
| `duration` | string | Coupon duration returned by Yotpo. |
| `icon` | string | Icon identifier for the redemption option. |
| `id` | number | Yotpo redemption option ID. |
| `name` | string | Display name of the redemption option. |
| `type` | string | Redemption option type. |
| `unrenderedDescription` | string | Raw redemption option description from Yotpo. |
| `unrenderedName` | string | Raw redemption option name from Yotpo. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/redemption_codes` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-coupon-codes.md) for the provider-specific parameters and requirements.

