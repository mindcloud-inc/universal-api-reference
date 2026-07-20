# Cursor: Launch Agent



```
POST https://connect.mindcloud.co/v1/universal/cursor/latest/actions/launch-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/launch-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt.text": "Add a README.md file with installation instructions"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursor/latest/actions/launch-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt.text": "Add a README.md file with installation instructions"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt.text` | string | yes | Task or instructions for the agent to execute. Example: `Add a README.md file with installation instructions`. |
| `source.repository` | string | no | GitHub repository URL for the agent to work in. Required unless using Source PR URL. Example: `https://github.com/your-org/your-repo`. |
| `source.ref` | string | no | Branch, tag, or commit hash to use as the base ref. Example: `main`. |
| `model` | string | no | Explicit model ID from List Models, or `default` to use Cursor's configured default. Default: `default`. Example: `default`. |
| `target.autoCreatePr` | boolean | no | Whether Cursor should automatically create a pull request when the agent completes. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `target.branchName` | string | no | Custom branch name for the agent to create. Example: `feature/add-readme`. |
| `source.prUrl` | string | no | GitHub pull request URL. When provided, Cursor works on the PR repository and branches. Example: `https://github.com/your-org/your-repo/pull/123`. |
| `target.openAsCursorGithubApp` | boolean | no | Open the pull request as the Cursor GitHub App. Only applies when Auto Create PR is true. Default: `false`. |
| `target.skipReviewerRequest` | boolean | no | Skip adding the user as reviewer when PR is opened by the Cursor GitHub App. Default: `false`. |
| `target.autoBranch` | boolean | no | Whether to create a new branch when Source PR URL is provided. Defaults to true. Default: `true`. |
| `webhook.url` | string | no | URL to receive agent status-change webhook notifications. Example: `https://example.com/webhooks/cursor-agent`. |
| `webhook.secret` | string | no | Secret for webhook payload verification, minimum 32 characters. Example: `minimum-32-character-secret`. |
| `prompt.images[]` | array<object> | no | Optional array of base64 encoded images, maximum 5. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "source": {
        "ref": "string",
        "repository": "string"
      },
      "status": "string",
      "target": {
        "autoCreatePr": true,
        "branchName": "Ava Chen",
        "openAsCursorGithubApp": true,
        "prUrl": "https://example.com",
        "skipReviewerRequest": true,
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the agent was created. |
| `id` | string | Unique cloud agent identifier. |
| `name` | string | Agent name. |
| `source.ref` | string | Git ref used as the base branch. |
| `source.repository` | string | GitHub repository URL. |
| `status` | string | Initial status of the newly created agent. |
| `target.autoCreatePr` | boolean | Whether Cursor will automatically create a pull request. |
| `target.branchName` | string | Git branch where the agent is working. |
| `target.openAsCursorGithubApp` | boolean | Whether the PR is opened by the Cursor GitHub App. |
| `target.prUrl` | string | Pull request URL, if any. |
| `target.skipReviewerRequest` | boolean | Whether reviewer request is skipped. |
| `target.url` | string | Cursor Web URL for the agent. |

## Native endpoint

Through the native Cursor API, this operation is `POST /v0/agents` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/launch-agent.md) for the provider-specific parameters and requirements.

