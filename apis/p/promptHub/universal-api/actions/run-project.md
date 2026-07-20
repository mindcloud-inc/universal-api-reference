# PromptHub: Run Project

Runs a PromptHub project by project ID.

```
POST https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/run-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/run-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/run-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The PromptHub project ID. |
| `variables` | object | no | Variable values to inject into the project request. |
| `prompt` | string | no | The final user message for chat projects. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch` | string | no | Run the head revision from a specific branch. |
| `hash` | string | no | Run a specific project revision hash. |
| `messages[]` | array<object> | no | Chat history messages for chat projects. |
| `metadata` | object | no | Metadata to associate with the PromptHub run. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PromptHub API returns.

## Native endpoint

Through the native PromptHub API, this operation is `POST /projects/:projectId/run` (base URL `https://app.prompthub.us/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-project.md) for the provider-specific parameters and requirements.

