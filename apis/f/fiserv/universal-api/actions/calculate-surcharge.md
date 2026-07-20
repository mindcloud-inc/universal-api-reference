# Fiserv: Calculate Surcharge

Calculates a surcharge for a payment in Fiserv.

```
POST https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/calculate-surcharge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/calculate-surcharge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xAccountId": "string",
  "paymentMethodId": "string",
  "amount": 1,
  "percent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/calculate-surcharge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xAccountId": "string",
    "paymentMethodId": "string",
    "amount": 1,
    "percent": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xAccountId` | string | yes | Merchant account ID required in the x-account-id header. |
| `paymentMethodId` | string | yes | Payment method ID used to calculate the surcharge. |
| `postalCode` | string | no | Postal code for the surcharge calculation. |
| `amount` | number | yes | Payment amount in minor units. |
| `percent` | number | yes | Surcharge percentage, from 0 to 3. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `POST /surcharge` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-surcharge.md) for the provider-specific parameters and requirements.

