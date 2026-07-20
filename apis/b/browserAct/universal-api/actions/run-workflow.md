# BrowserAct: Run Workflow

Creates a new task in BrowserAct from a workflow.

```
POST https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/run-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/run-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/run-workflow', {
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
| `workflowId` | string | yes | The published BrowserAct workflow ID to run. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputParametersJson` | string | no | Optional JSON array of {"name","value"} objects matching the workflow input parameters. |
| `saveBrowserData` | boolean | no | Whether BrowserAct should return a reusable browser profile for this run. |
| `profileId` | string | no | Optional BrowserAct profile ID to reuse cookies and browser state. |
| `callbackUrl` | string | no | Optional webhook URL to receive the completed task result. |
| `statusChangeCallbackUrl` | string | no | Optional webhook URL to receive task status change events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "profileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The created BrowserAct task ID. |
| `profileId` | string | Returned browser profile ID when BrowserAct provides one. |

## Native endpoint

Through the native BrowserAct API, this operation is `POST /run-task` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-workflow.md) for the provider-specific parameters and requirements.

