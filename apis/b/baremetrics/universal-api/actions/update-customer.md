# Baremetrics: Update Customer

Updates a customer in Baremetrics.

```
PUT https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerOid": "customer_1",
  "sourceId": "source_1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerOid": "customer_1",
    "sourceId": "source_1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerOid` | string | yes | Your unique ID for the customer Example: `customer_1`. |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `name` | string | no | Example: `Example Name`. |
| `notes` | string | no |  |
| `created` | string | no | Unix timestamp of when this customer was created |
| `email` | string | no | Email for this customer Example: `customer@example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `PUT /v1/:source_id/customers/:customer_oid` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

