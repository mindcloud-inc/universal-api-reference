# RocketReach: Bulk Lookup People

Creates a RocketReach bulk people lookup.

```
POST https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-people', {
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
| `profile_list` | string | no |  |
| `queries[]` | array<object> | no | List of profile lookup queries for between 10 and 100 profiles. |
| `queries[].current_employer` | string | no |  |
| `queries[].email` | string | no |  |
| `queries[].id` | number | no |  |
| `queries[].linkedin_url` | string | no |  |
| `queries[].lookup_type` | string | no | Lookup type for the person lookup query. |
| `queries[].name` | string | no |  |
| `queries[].npi_number` | number | no | National Provider Identifier for the person lookup query. |
| `queries[].title` | string | no | Job title for the person lookup query. |
| `webhook_id` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RocketReach API returns.

## Native endpoint

Through the native RocketReach API, this operation is `POST /bulkLookup` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-lookup-people.md) for the provider-specific parameters and requirements.

