# Bitbucket: Delete Repository

Deletes a repository from Bitbucket.

```
DELETE https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/delete-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/delete-repository?connectionId=$CONNECTION_ID&workspace=string&repo_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace": "string",
  "repo_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/delete-repository?${params}`, {
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
| `workspace` | string | yes | Workspace slug that owns the repository. |
| `repo_slug` | string | yes | Repository slug to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bitbucket API, this operation is `DELETE /repositories/:workspace/:repo_slug` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-repository.md) for the provider-specific parameters and requirements.

