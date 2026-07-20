# Process Street: Create Workflow Run



```
POST https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/create-workflow-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/create-workflow-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/create-workflow-run', {
  method: 'POST',
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
| `workflowId` | string | yes | The ID of the workflow to run. |
| `name` | string | no | The name of the new workflow run. |
| `dueDate` | date | no | Optional due date for the new workflow run. |
| `shared` | boolean | no | Whether the workflow run should be shared. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "links": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `links` | array<object> |  |

## Native endpoint

Through the native Process Street API, this operation is `POST /workflow-runs` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow-run.md) for the provider-specific parameters and requirements.

