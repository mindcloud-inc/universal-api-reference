# BrowserAct: Retrieve Workflow

Retrieves a workflow from BrowserAct.

```
GET https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-workflow?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/retrieve-workflow?${params}`, {
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
| `workflowId` | string | yes | Workflow ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "publishAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createAt` | string | Workflow creation timestamp. |
| `description` | string | Workflow description. |
| `id` | string | Workflow ID. |
| `name` | string | Workflow name. |
| `publishAt` | string | Workflow publish timestamp. |

## Native endpoint

Through the native BrowserAct API, this operation is `GET /get-workflow` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-workflow.md) for the provider-specific parameters and requirements.

