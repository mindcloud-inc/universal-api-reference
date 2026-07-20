# Vouchery.io: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categories": "string",
  "identifier": "string",
  "metadata": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categories": "string",
    "identifier": "string",
    "metadata": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categories` | string | yes | Customer categories as a JSON array string. |
| `email` | string | no | Updated customer email. |
| `identifier` | string | yes | Customer identifier from Vouchery. |
| `loyaltyPoints` | number | no | Updated loyalty points total. |
| `metadata` | string | yes | Customer metadata as a JSON object string. |
| `name` | string | no | Updated customer name. |
| `referralCode` | string | no | Updated referral code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `PUT /customers/:identifier` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

