# Skyvern: Create Script

Creates a new script in Skyvern.

```
POST https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/create-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/create-script" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/create-script', {
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
| `files` | string | no | Array of files to include in the script |
| `runId` | string | no | Associated run ID |
| `workflowId` | string | no | Associated workflow ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "file_count": 1,
      "file_tree": {},
      "run_id": "string",
      "script_id": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Script creation timestamp |
| `file_count` | number | Total number of files in the script |
| `file_tree` | object | Hierarchical file tree structure |
| `run_id` | string | Workflow or task run ID that generated the script |
| `script_id` | string | Unique script identifier |
| `version` | number | Script version number |

## Native endpoint

Through the native Skyvern API, this operation is `POST /v1/scripts` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-script.md) for the provider-specific parameters and requirements.

