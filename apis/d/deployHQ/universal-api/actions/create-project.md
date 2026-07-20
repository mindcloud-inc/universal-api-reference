# DeployHQ: Create Project

Creates a new project in DeployHQ.

```
POST https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | object | yes | Project payload. DeployHQ accepts fields such as name, keypair_identifier, zone_id, and template_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_url": "https://example.com",
      "auto_deploy_url": "https://example.com",
      "build_commands_url": "https://example.com",
      "config_files_url": "https://example.com",
      "deployments_url": "https://example.com",
      "environment_variables_url": "https://example.com",
      "identifier": "string",
      "last_deployed_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "public_key": "string",
      "repository": "string",
      "repository_url": "https://example.com",
      "servers_url": "https://example.com",
      "url": "https://example.com",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_url` | string |  |
| `auto_deploy_url` | string |  |
| `build_commands_url` | string |  |
| `config_files_url` | string |  |
| `deployments_url` | string |  |
| `environment_variables_url` | string |  |
| `identifier` | string |  |
| `last_deployed_at` | date |  |
| `name` | string |  |
| `permalink` | string |  |
| `public_key` | string |  |
| `repository` | string |  |
| `repository_url` | string |  |
| `servers_url` | string |  |
| `url` | string |  |
| `zone` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `POST /projects` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

