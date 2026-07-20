# DeployHQ: Get Project

Retrieves a project from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | The identifier or permalink of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_url": "https://example.com",
      "auto_deploy_url": "https://example.com",
      "build_commands_url": "https://example.com",
      "capabilities": [
        {}
      ],
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
      "starred": true,
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
| `capabilities` | array<object> |  |
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
| `starred` | boolean |  |
| `url` | string |  |
| `zone` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `GET /projects/:id` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

