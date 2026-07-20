# ApproveThis: Create Workflow

Creates a workflow from an ApproveThis template.

```
POST https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": "mindcloud-template-probe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": "mindcloud-template-probe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | string | yes | The template slug. Example: `mindcloud-template-probe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "templateId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `templateId` | number |  |

## Native endpoint

Through the native ApproveThis API, this operation is `POST /templates/:template/workflow` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

