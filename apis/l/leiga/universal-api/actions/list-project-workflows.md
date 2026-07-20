# Leiga: List Project Workflows

Retrieves workflows for a project in Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-workflows?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-workflows?${params}`, {
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
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultValue": true,
      "id": 1,
      "issueTypes": [
        {}
      ],
      "states": [
        {}
      ],
      "workflowDesc": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultValue` | boolean | Whether this is the default workflow. |
| `id` | number | Workflow ID. |
| `issueTypes` | array<object> | Related issue types. |
| `states` | array<object> | Workflow states. |
| `workflowDesc` | string | Workflow description. |
| `workflowName` | string | Workflow name. |

## Native endpoint

Through the native Leiga API, this operation is `POST /workflow/list` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-workflows.md) for the provider-specific parameters and requirements.

