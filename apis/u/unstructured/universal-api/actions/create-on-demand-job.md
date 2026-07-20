# Unstructured: Create On-Demand Job

Creates an on-demand job in Unstructured.

```
POST https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-on-demand-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-on-demand-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-on-demand-job', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "inputFileIds": [
        [
          "string"
        ]
      ],
      "jobType": "string",
      "outputNodeFiles": [
        [
          {}
        ]
      ],
      "runtime": "string",
      "status": "string",
      "workflowId": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `id` | string | Job ID. |
| `inputFileIds[]` | array<string> | Input file IDs. |
| `jobType` | string | Job type. |
| `outputNodeFiles[]` | array<object> | Output node files. |
| `runtime` | string | Job runtime duration. |
| `status` | string | Job status. |
| `workflowId` | string | Workflow ID. |
| `workflowName` | string | Workflow name. |

## Native endpoint

Through the native Unstructured API, this operation is `POST /jobs/` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-on-demand-job.md) for the provider-specific parameters and requirements.

