# Routee: Delete a number from a pool

Removes a number from a pool in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-a-number-from-a-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-a-number-from-a-pool?connectionId=$CONNECTION_ID&poolid=string&poolId=string&msisdn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolid": "string",
  "poolId": "string",
  "msisdn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/delete-a-number-from-a-pool?${params}`, {
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
| `poolid` | string | yes | The tracking id of the pool. |
| `poolId` | string | yes |  |
| `msisdn` | string | yes | The number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `DELETE /pools/my/:poolId/numbers/:msisdn` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-number-from-a-pool.md) for the provider-specific parameters and requirements.

