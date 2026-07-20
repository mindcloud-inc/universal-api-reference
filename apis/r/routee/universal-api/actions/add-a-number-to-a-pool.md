# Routee: Add a Number to a pool

Adds a number to a pool in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-a-number-to-a-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-a-number-to-a-pool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdn": "string",
  "poolId": "string",
  "poolid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-a-number-to-a-pool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msisdn": "string",
    "poolId": "string",
    "poolid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdn` | string | yes | The number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |
| `poolId` | string | yes |  |
| `poolid` | string | yes | The tracking id of the pool. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `PUT /pools/my/:poolId/numbers/:msisdn` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-number-to-a-pool.md) for the provider-specific parameters and requirements.

