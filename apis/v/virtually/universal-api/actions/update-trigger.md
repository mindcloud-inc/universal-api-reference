# Virtually: Update Trigger

Updates an existing trigger in Virtually.

```
PUT https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-trigger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-trigger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "triggerId": "string",
  "clauses[]": [
    {}
  ],
  "clauses[].event": "string",
  "clauses[].comparisonOp": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-trigger', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "triggerId": "string",
    "clauses[]": [{}],
    "clauses[].event": "string",
    "clauses[].comparisonOp": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `triggerId` | string | yes |  |
| `clauses[]` | array<object> | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |
| `logicalOp` | string | no | Default: `and`. |
| `clauses[].props` | object | no |  |
| `clauses[].props.includeNonRequired` | boolean | no |  |
| `clauses[].event` | string | yes |  |
| `clauses[].props.path` | string | no |  |
| `clauses[].props.aggregation` | string | no |  |
| `clauses[].quantity` | number | no |  |
| `clauses[].comparisonOp` | string | yes |  |
| `clauses[].trailingDays` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtually API returns.

## Native endpoint

Through the native Virtually API, this operation is `PATCH /api/v2/orgs/:orgId/triggers/:triggerId` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-trigger.md) for the provider-specific parameters and requirements.

