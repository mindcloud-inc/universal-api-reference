# DeployHQ: Update Repository

Updates the repository for a project in DeployHQ.

```
PUT https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/update-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/update-repository" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "repository": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/update-repository', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "repository": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The identifier or permalink of the project. |
| `repository` | object | yes | Repository settings payload. DeployHQ accepts fields such as url, scm_type, protocol, username, password, branch, port, root_path, hosting_service_type, and manual_config. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "cached": true,
      "hosting_service": {},
      "port": 1,
      "scm_type": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `cached` | boolean |  |
| `hosting_service` | object |  |
| `port` | number |  |
| `scm_type` | string |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `PATCH /projects/:project_id/repository` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-repository.md) for the provider-specific parameters and requirements.

