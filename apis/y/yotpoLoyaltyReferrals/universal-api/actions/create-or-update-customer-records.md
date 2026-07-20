# Yotpo Loyalty & Referrals: Create or Update Customer Records

Creates or updates customer records in Yotpo Loyalty & Referrals.

```
PUT https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-or-update-customer-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-or-update-customer-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-or-update-customer-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The customer's email address. |
| `id` | string | no | The identifier used to uniquely identify the customer in your system. |
| `firstName` | string | no | The customer's first name. |
| `lastName` | string | no | The customer's last name. |
| `phoneNumber` | string | no | The customer's phone number in E.164 format. |
| `hasAccount` | boolean | no | Whether the customer has an account with the eCommerce platform. |
| `optedIn` | boolean | no | Whether the customer should be opted in to the loyalty program. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryIsoCode` | string | no | Use only if phone number cannot be sent in full E.164 format. |
| `platformAccountCreatedAt` | string | no | Date and time when the customer created an account with your store. |
| `posAccountId` | string | no | The point-of-sale unique account identifier. |
| `tags` | string | no | A comma-separated list of tags or collections this customer belongs to. This overwrites existing tags. |
| `optedInAt` | string | no | Date and time when the customer was opted in to the loyalty program. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yotpo Loyalty & Referrals API returns.

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/customers` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer-records.md) for the provider-specific parameters and requirements.

