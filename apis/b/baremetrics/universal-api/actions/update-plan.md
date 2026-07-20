# Baremetrics: Update Plan

Updates a plan in Baremetrics.

```
PUT https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baremetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "planOid": "plan_1",
  "sourceId": "source_1",
  "name": "Example Name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/update-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "planOid": "plan_1",
    "sourceId": "source_1",
    "name": "Example Name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planOid` | string | yes | Your interval plan id Example: `plan_1`. |
| `sourceId` | string | yes | Please see [Sources](ref:sources) Example: `source_1`. |
| `name` | string | yes | The new name of this plan Example: `Example Name`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baremetrics API returns.

## Native endpoint

Through the native Baremetrics API, this operation is `PUT /v1/:source_id/plans/:plan_oid` (base URL `https://sandbox.baremetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-plan.md) for the provider-specific parameters and requirements.

