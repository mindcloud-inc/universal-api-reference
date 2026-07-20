# Socket: Delete Repository

Deletes an existing repository from Socket.

```
DELETE https://connect.mindcloud.co/v1/universal/socket/latest/actions/delete-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/socket/latest/actions/delete-repository?connectionId=$CONNECTION_ID&repoSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repoSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/delete-repository?${params}`, {
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
| `workspace` | string | no |  |
| `repoSlug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Socket API, this operation is `DELETE /orgs/:org_slug/repos/:repo_slug` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-repository.md) for the provider-specific parameters and requirements.

