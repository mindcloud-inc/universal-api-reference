# ServiceTitan: Create Payment

Creates a new payment in ServiceTitan.

```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no |  |
| `paymentTypeId` | string | no |  |
| `amount` | string | no |  |
| `date` | string | no |  |
| `checkNumber` | string | no |  |
| `referenceNumber` | string | no |  |
| `memo` | string | no |  |
| `syncStatus` | string | no |  |
| `customFields[]` | array<object> | no | ServiceTitan payment custom fields. Use VistaID type 13614166 to store the Vista receipt identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST accounting/v2/tenant/{{credentials.tenant}}/payments` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

