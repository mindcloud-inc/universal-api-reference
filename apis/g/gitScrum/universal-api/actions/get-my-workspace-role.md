# GitScrum: Get My Workspace Role

Retrieves your role in a GitScrum workspace.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-my-workspace-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-my-workspace-role?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-my-workspace-role?${params}`, {
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
| `slug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can_create_project": 1,
      "is_admin": 1,
      "is_owner": true,
      "is_workspace_owner": true,
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_create_project` | number |  |
| `is_admin` | number |  |
| `is_owner` | boolean |  |
| `is_workspace_owner` | boolean |  |
| `role` | string |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /companies/:slug/my-role` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-workspace-role.md) for the provider-specific parameters and requirements.

