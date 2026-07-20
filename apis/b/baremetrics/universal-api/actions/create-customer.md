# Baremetrics: Create Customer

Creates a customer in Baremetrics.

```
POST https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "source_1",
  "oid": "resource_1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "source_1",
    "oid": "resource_1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `name` | string | no | Example: `Example Name`. |
| `notes` | string | no | Your own notes for this customer. These will be displayed in the profile |
| `email` | string | no | An email address for this customer. This is used to lookup extra profile information Example: `customer@example.com`. |
| `oid` | string | yes | Your unique ID for the customer Example: `resource_1`. |
| `created` | string | no | A unix timestamp of when this customer was created. Defaults to now. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `POST /v1/:source_id/customers` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

