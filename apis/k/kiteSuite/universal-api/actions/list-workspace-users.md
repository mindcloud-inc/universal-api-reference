# KiteSuite: List Workspace Users

Retrieves workspace users from KiteSuite.

```
GET https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-users?${params}`, {
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
| `id` | string | yes | Workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "selectedWorkspace": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `selectedWorkspace` | string |  |
| `status` | string |  |

## Native endpoint

Through the native KiteSuite API, this operation is `GET /api/v1/user/workspace/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-users.md) for the provider-specific parameters and requirements.

