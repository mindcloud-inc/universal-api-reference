# DeployHQ: Get Deployment

Retrieves a deployment from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-deployment?connectionId=$CONNECTION_ID&projectId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-deployment?${params}`, {
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
| `projectId` | string | yes | The identifier or permalink of the project. |
| `id` | string | yes | The identifier of the deployment. |

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

Through the native DeployHQ API, this operation is `GET /projects/:project_id/deployments/:id` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment.md) for the provider-specific parameters and requirements.

