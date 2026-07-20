# Mem0: List Project Members

Retrieves project members from Mem0.

```
GET https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-project-members?connectionId=$CONNECTION_ID&org_id=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-project-members?${params}`, {
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
| `org_id` | string | yes | Mem0 organization ID from the project member resource path. |
| `project_id` | string | yes | Mem0 project ID from the project member resource path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": [
        {}
      ],
      "role": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `members` | array<object> |  |
| `role` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Mem0 API, this operation is `GET /api/v1/orgs/organizations/:org_id/projects/:project_id/members/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-members.md) for the provider-specific parameters and requirements.

