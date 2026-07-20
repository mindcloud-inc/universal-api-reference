# Range: List Org Users

List organization users with optional team and relation filters.

```
GET https://connect.mindcloud.co/v1/universal/range/latest/actions/list-org-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/list-org-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/list-org-users?${params}`, {
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
| `forUserId` | string | no | Fetch users on teams this user is related to. |
| `limit` | number | no | Maximum number of users to return. |
| `orgId` | string | no | The Range organization ID. |
| `teamId` | string | no | Filter users to a specific team. |
| `userIds` | string | no | Explicit user IDs to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `users` | array<object> |  |

## Native endpoint

Through the native Range API, this operation is `GET /v1/orgs/:orgId/users` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-org-users.md) for the provider-specific parameters and requirements.

