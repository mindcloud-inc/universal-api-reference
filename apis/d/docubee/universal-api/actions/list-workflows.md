# Docubee: List Workflows

Retrieves workflows from Docubee.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-workflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "instanceCount": 1,
      "name": "Ava Chen",
      "runningInstances": 1,
      "state": "string",
      "templateId": "string",
      "tenantId": "string",
      "wfModelId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The workflow template description. |
| `instanceCount` | number | The number of instances created from this template. |
| `name` | string | The workflow template name. |
| `runningInstances` | number | The number of running instances for this template. |
| `state` | string | The workflow template state. |
| `templateId` | string | The workflow template ID. |
| `tenantId` | string | The Docubee tenant ID. |
| `wfModelId` | string | The workflow model ID. |

## Native endpoint

Through the native Docubee API, this operation is `GET /workflowTemplates` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

