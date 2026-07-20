# Cryotos: List Template Histories By Workflow ID



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-template-histories-by-workflow-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-template-histories-by-workflow-id?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-template-histories-by-workflow-id?${params}`, {
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
| `workflowId` | string | yes | The workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "creationDate": "string",
      "id": 1,
      "reportQuerySchema": "string",
      "templateId": 1,
      "templateName": "Ava Chen",
      "templateSchema": "string",
      "templateVersion": 1,
      "templateWorkflowId": 1,
      "templateWorkflowName": "Ava Chen",
      "updationDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `creationDate` | string |  |
| `id` | number |  |
| `reportQuerySchema` | string |  |
| `templateId` | number |  |
| `templateName` | string |  |
| `templateSchema` | string |  |
| `templateVersion` | number |  |
| `templateWorkflowId` | number |  |
| `templateWorkflowName` | string |  |
| `updationDate` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/template-histories/findByWorkflowId/:workflowId` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-histories-by-workflow-id.md) for the provider-specific parameters and requirements.

