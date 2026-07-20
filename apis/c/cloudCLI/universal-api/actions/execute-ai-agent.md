# Cloud CLI: Execute AI Agent

Runs an AI agent in a Cloud CLI environment.

```
POST https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/execute-ai-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud CLI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/execute-ai-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentId": "46ce370c-f611-40e0-9764-ed0032dc76fa",
  "projectName": "hello-world",
  "message": "Add a README note saying the environment is ready."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/execute-ai-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentId": "46ce370c-f611-40e0-9764-ed0032dc76fa",
    "projectName": "hello-world",
    "message": "Add a README note saying the environment is ready."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environmentId` | string | yes | ID of the running environment. Example: `46ce370c-f611-40e0-9764-ed0032dc76fa`. |
| `projectName` | string | yes | Project folder name inside /workspace. Example: `hello-world`. |
| `message` | string | yes | Task description for the AI agent. Example: `Add a README note saying the environment is ready.`. |
| `provider` | string | no | AI provider to use. One of: `0`, `1`, `2`. Default: `claude`. Example: `claude`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | no | Provider-specific model name. Example: `sonnet`. |
| `createBranch` | boolean | no | Create a git branch for the changes. Default: `false`. |
| `createPR` | boolean | no | Create a pull request after completion. Default: `false`. |
| `githubToken` | string | no | GitHub token for private repositories or pull request creation. Example: `ghp_xxxxxxxxxxxx`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud CLI API returns.

## Native endpoint

Through the native Cloud CLI API, this operation is `POST /agent/execute` (base URL `https://cloudcli.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-ai-agent.md) for the provider-specific parameters and requirements.

