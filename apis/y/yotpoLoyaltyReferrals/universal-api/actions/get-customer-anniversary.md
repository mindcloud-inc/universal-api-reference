# Yotpo Loyalty & Referrals: Get Customer Anniversary

Retrieves a customer's anniversary from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-customer-anniversary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-customer-anniversary?connectionId=$CONNECTION_ID&customerEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/get-customer-anniversary?${params}`, {
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
| `customerEmail` | string | yes | The customer's email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "day": 1,
      "month": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `day` | number | Customer anniversary day of month. |
| `month` | number | Customer anniversary month. |
| `year` | number | Customer anniversary year when available. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/customer_anniversary` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-anniversary.md) for the provider-specific parameters and requirements.

