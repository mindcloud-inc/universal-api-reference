# BugHerd: List User Projects

Retrieves projects for a BugHerd user.

```
GET https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-user-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-user-projects?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/list-user-projects?${params}`, {
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
| `userId` | number | yes | The BugHerd user ID. |
| `createdSince` | string | no | Return projects created after this timestamp. |
| `isActive` | boolean | no | Filter by active status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "ownerName": "Ava Chen",
      "sites": [
        "string"
      ],
      "tasks": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `name` | string |  |
| `ownerName` | string |  |
| `sites` | array<string> |  |
| `tasks` | boolean |  |

## Native endpoint

Through the native BugHerd API, this operation is `GET users/:user_id/projects.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-projects.md) for the provider-specific parameters and requirements.

