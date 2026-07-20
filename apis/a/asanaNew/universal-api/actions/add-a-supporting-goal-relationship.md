# Asana: Add a supporting goal relationship

Adds a supporting goal relationship in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-supporting-goal-relationship
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-supporting-goal-relationship" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataContributionWeight": 1,
  "dataInsertAfter": "string",
  "dataInsertBefore": "string",
  "dataSupportingResource": "string",
  "goalGid": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-supporting-goal-relationship', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataContributionWeight": 1,
    "dataInsertAfter": "string",
    "dataInsertBefore": "string",
    "dataSupportingResource": "string",
    "goalGid": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataContributionWeight` | number | yes |  |
| `dataInsertAfter` | string | yes |  |
| `dataInsertBefore` | string | yes |  |
| `dataSupportingResource` | string | yes |  |
| `goalGid` | string | yes | Path parameter: goal_gid |
| `optFields[]` | array<string> | no |  |
| `data` | object | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST goals/:goal_gid/addSupportingRelationship` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-supporting-goal-relationship.md) for the provider-specific parameters and requirements.

