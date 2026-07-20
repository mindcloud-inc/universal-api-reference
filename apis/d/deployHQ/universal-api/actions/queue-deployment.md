# DeployHQ: Queue Deployment

Creates a deployment for a project in DeployHQ.

```
POST https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/queue-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/queue-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "deployment": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/queue-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "deployment": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The identifier or permalink of the project. |
| `deployment` | object | yes | Deployment payload. DeployHQ accepts fields such as branch, mode, start_revision, end_revision, parent_identifier, server_identifier, run_build_commands, use_latest, and skip_if_not_changes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schedule` | object | no | Optional schedule payload for future, daily, weekly, monthly, or custom deployment scheduling. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archived_at": "2026-05-07T12:00:00.000Z",
      "branch": "string",
      "config_files_deployment": true,
      "configuration": {},
      "deferred": true,
      "deployer": "string",
      "deployer_avatar": "string",
      "end_revision": {},
      "files": {},
      "identifier": "string",
      "legacy": true,
      "log_summary": "string",
      "metadata": {},
      "overview": "string",
      "project": {},
      "servers": [
        {}
      ],
      "start_revision": {},
      "status": "string",
      "steps": [
        {}
      ],
      "timestamps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archived_at` | date |  |
| `branch` | string |  |
| `config_files_deployment` | boolean |  |
| `configuration` | object |  |
| `deferred` | boolean |  |
| `deployer` | string |  |
| `deployer_avatar` | string |  |
| `end_revision` | object |  |
| `files` | object |  |
| `identifier` | string |  |
| `legacy` | boolean |  |
| `log_summary` | string |  |
| `metadata` | object |  |
| `overview` | string |  |
| `project` | object |  |
| `servers` | array<object> |  |
| `start_revision` | object |  |
| `status` | string |  |
| `steps` | array<object> |  |
| `timestamps` | object |  |

## Native endpoint

Through the native DeployHQ API, this operation is `POST /projects/:project_id/deployments` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-deployment.md) for the provider-specific parameters and requirements.

