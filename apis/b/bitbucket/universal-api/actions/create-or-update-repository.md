# Bitbucket: Create Or Update Repository

Creates or updates a repository in Bitbucket.

```
POST https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/create-or-update-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/create-or-update-repository" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace": "string",
  "repo_slug": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/create-or-update-repository', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace": "string",
    "repo_slug": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace` | string | yes | Workspace slug that owns the repository. |
| `repo_slug` | string | yes | Repository slug to create or update. |
| `name` | string | yes | Human-readable repository name. |
| `description` | string | no | Repository description. |
| `is_private` | boolean | no | Whether the repository should be private. |
| `project_key` | string | no | Bitbucket project key for the repository. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "full_name": "Ava Chen",
      "is_private": true,
      "language": "string",
      "name": "Ava Chen",
      "slug": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `full_name` | string |  |
| `is_private` | boolean |  |
| `language` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Bitbucket API, this operation is `PUT /repositories/:workspace/:repo_slug` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-repository.md) for the provider-specific parameters and requirements.

