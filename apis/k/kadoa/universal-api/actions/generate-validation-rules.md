# Kadoa: Generate Validation Rules



```
POST https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/generate-validation-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/generate-validation-rules" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userPrompt": "string",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/generate-validation-rules', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userPrompt": "string",
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userPrompt` | string | yes | Description of rules to generate |
| `workflowId` | string | yes | Workflow ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `selectedColumns` | string | no | JSON array of columns |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kadoa API returns.

## Native endpoint

Through the native Kadoa API, this operation is `POST /v4/data-validation/rules/actions/generate` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-validation-rules.md) for the provider-specific parameters and requirements.

