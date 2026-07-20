# ApproveThis: Get Workflow

Retrieves a workflow from ApproveThis by ID.

```
GET https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/get-workflow?connectionId=$CONNECTION_ID&workflow=a19b71e5-d0c2-459d-b34a-612a9f8438d1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflow": "a19b71e5-d0c2-459d-b34a-612a9f8438d1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/get-workflow?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflow` | string | yes | The workflow ID. Example: `a19b71e5-d0c2-459d-b34a-612a9f8438d1`. |

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

Through the native ApproveThis API, this operation is `GET /workflows/:workflow` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

