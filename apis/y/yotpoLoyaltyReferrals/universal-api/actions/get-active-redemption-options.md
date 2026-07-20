# Yotpo Loyalty & Referrals: Get Active Redemption Options

Retrieves active redemption options from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-active-redemption-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-active-redemption-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-active-redemption-options?${params}`, {
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
| `isOffline` | string | no | Filter redemption options by offline availability. |
| `customerEmail` | string | no | Filter redemption options for a specific customer email. |
| `customerId` | string | no | Filter redemption options for a specific customer ID. |
| `phoneNumber` | string | no | Filter redemption options for a specific phone number. |
| `discountType` | string | no | Filter redemption options by discount type. |

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

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/redemption_options` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-redemption-options.md) for the provider-specific parameters and requirements.

