# Yotpo Loyalty & Referrals: Set Customer Birthday

Updates a customer's birthday in Yotpo Loyalty & Referrals.

```
PUT https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/set-customer-birthday
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/set-customer-birthday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "day": 1,
  "month": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/set-customer-birthday', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "day": 1,
    "month": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerEmail` | string | no | The customer's email address. Provide this or Customer ID. |
| `customerId` | string | no | The identifier used to uniquely identify the customer in your system. Provide this or Customer Email. |
| `day` | number | yes | The day of the month for the customer's birthday. |
| `month` | number | yes | The month of the year for the customer's birthday. |
| `year` | number | no | The optional year for the customer's birthday. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yotpo Loyalty & Referrals API returns.

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/customer_birthdays` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-customer-birthday.md) for the provider-specific parameters and requirements.

