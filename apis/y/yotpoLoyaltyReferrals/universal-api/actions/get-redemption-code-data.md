# Yotpo Loyalty & Referrals: Get Redemption Code Data

Retrieves redemption code data from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-redemption-code-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-redemption-code-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-redemption-code-data?${params}`, {
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
| `thirdPartyId` | string | no | Third-party unique identifier for the redemption code. |
| `code` | string | no | Discount code to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "email": "ava@example.com",
      "id": 1,
      "pointRedemptionId": 1,
      "thirdPartyId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Generated redemption code. |
| `email` | string | Email address associated with the redemption code. |
| `id` | number | Unique identifier of the redemption-code record. |
| `pointRedemptionId` | number | Point redemption identifier associated with the code. |
| `thirdPartyId` | string | Third-party identifier for the code, when available. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/redemption_codes` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redemption-code-data.md) for the provider-specific parameters and requirements.

