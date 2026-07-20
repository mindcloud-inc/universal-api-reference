# Virtually: Create Trigger

Creates a new trigger in Virtually.

```
POST https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-trigger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-trigger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clauses[]": [
    {}
  ],
  "logicalOp": "and",
  "clauses[].event": "string",
  "clauses[].quantity": 1,
  "clauses[].comparisonOp": "string",
  "clauses[].trailingDays": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-trigger', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clauses[]": [{}],
    "logicalOp": "and",
    "clauses[].event": "string",
    "clauses[].quantity": 1,
    "clauses[].comparisonOp": "string",
    "clauses[].trailingDays": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags[]` | array<string> | no |  |
| `excludeTags[]` | array<string> | no |  |
| `clauses[]` | array<object> | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |
| `logicalOp` | string | yes | Default: `and`. |
| `createdBy` | string | no |  |
| `clauses[].props` | object | no |  |
| `clauses[].props.includeNonRequired` | boolean | no |  |
| `clauses[].event` | string | yes |  |
| `clauses[].quantity` | number | yes |  |
| `clauses[].comparisonOp` | string | yes |  |
| `clauses[].trailingDays` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "report": {},
      "trigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report` | object | Trigger creation report |
| `trigger` | object | Created trigger |

## Native endpoint

Through the native Virtually API, this operation is `POST /api/v2/orgs/:orgId/triggers` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-trigger.md) for the provider-specific parameters and requirements.

