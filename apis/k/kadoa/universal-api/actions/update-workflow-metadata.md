# Kadoa: Update Workflow Metadata



```
PUT https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-workflow-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-workflow-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/update-workflow-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | Workflow ID |
| `name` | string | no | Workflow name |
| `description` | string | no | Description |
| `tags` | string | no | JSON array of tags |
| `updateInterval` | string | no | Interval: ONLY_ONCE, HOURLY, DAILY, WEEKLY, MONTHLY, CUSTOM |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxPages` | number | no | Max pages |
| `maxDepth` | number | no | Max depth |
| `navigationMode` | string | no | Navigation mode |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kadoa API returns.

## Native endpoint

Through the native Kadoa API, this operation is `PUT /v4/workflows/:workflowId/metadata` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow-metadata.md) for the provider-specific parameters and requirements.

