# Socket: Create Repository

Creates a new repository in Socket.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-repository" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-repository', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | boolean | no | Default: `false`. |
| `defaultBranch` | string | no |  |
| `description` | string | no |  |
| `homepage` | string | no |  |
| `name` | string | yes |  |
| `visibility` | string | no |  |
| `workspace` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "defaultBranch": "string",
      "description": "string",
      "headFullScanId": "string",
      "homepage": "string",
      "id": "string",
      "integrationMeta": {
        "type": "string",
        "value": {
          "installationId": "string",
          "installationLogin": "string",
          "repoId": "string",
          "repoName": "Ava Chen"
        }
      },
      "name": "Ava Chen",
      "slug": "string",
      "updatedAt": "string",
      "visibility": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the repository is archived or not |
| `createdAt` | string | The creation date of the repository |
| `defaultBranch` | string | The default branch of the repository |
| `description` | string | The description of the repository |
| `headFullScanId` | string | The ID of the head full scan of the repository |
| `homepage` | string | The homepage URL of the repository |
| `id` | string | The ID of the repository |
| `integrationMeta` | object |  |
| `integrationMeta.type` | string |  |
| `integrationMeta.value` | object |  |
| `integrationMeta.value.installationId` | string | The GitHub installation_id of the active associated Socket GitHub App |
| `integrationMeta.value.installationLogin` | string | The GitHub login name that the active Socket GitHub App installation is installed to |
| `integrationMeta.value.repoId` | string | The id of the associated GitHub repo. |
| `integrationMeta.value.repoName` | string | The name of the associated GitHub repo. |
| `name` | string | The name of the repository |
| `slug` | string | The slug of the repository |
| `updatedAt` | string | The last update date of the repository |
| `visibility` | string | The visibility of the repository |
| `workspace` | string | The workspace of the repository |

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/repos` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-repository.md) for the provider-specific parameters and requirements.

