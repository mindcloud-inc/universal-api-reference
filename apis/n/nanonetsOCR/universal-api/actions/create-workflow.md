# Nanonets OCR: Create Workflow



```
POST https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/create-workflow', {
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
| `workflowType` | string | no | Workflow type identifier from Get Available Workflow Types. Example: `invoice`. |
| `description` | string | no | Description for the new workflow. Example: `Process invoices for AP review`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "settings": {
        "tableCapture": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `settings.tableCapture` | boolean |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `POST /workflows` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

