# SmartSuite: Duplicate Solution

Creates a duplicate of a solution in SmartSuite.

```
POST https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/duplicate-solution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/duplicate-solution" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "solutionId": "69b8536ce12736e94d922d88",
  "name": "MC Test Solution Copy 20260316",
  "fromWorkspace": "s1jqk8a8",
  "toWorkspace": "s1jqk8a8"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/duplicate-solution', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "solutionId": "69b8536ce12736e94d922d88",
    "name": "MC Test Solution Copy 20260316",
    "fromWorkspace": "s1jqk8a8",
    "toWorkspace": "s1jqk8a8"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `solutionId` | string | yes | The SmartSuite solution ID to duplicate. Example: `69b8536ce12736e94d922d88`. |
| `name` | string | yes | The name for the duplicated SmartSuite solution. Example: `MC Test Solution Copy 20260316`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromWorkspace` | string | yes | The source SmartSuite workspace ID. Example: `s1jqk8a8`. |
| `toWorkspace` | string | yes | The destination SmartSuite workspace ID. Example: `s1jqk8a8`. |
| `copyRecords` | boolean | no | Whether SmartSuite should copy records into the duplicated solution. Example: `false`. |
| `copyComments` | boolean | no | Whether SmartSuite should copy comments into the duplicated solution. Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SmartSuite API returns.

## Native endpoint

Through the native SmartSuite API, this operation is `POST /solutions/duplicate/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-solution.md) for the provider-specific parameters and requirements.

