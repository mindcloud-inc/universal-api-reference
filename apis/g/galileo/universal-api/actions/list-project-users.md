# Galileo: List Project Users

Finds user collaborators for a Galileo project.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-project-users?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/list-project-users?${params}`, {
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
| `projectId` | string | yes | Galileo project UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collaborators": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "permissions": [
            {
              "action": "string",
              "allowed": true,
              "message": "string"
            }
          ],
          "role": "string",
          "userId": "string"
        }
      ],
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "startingToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collaborators` | array<object> |  |
| `collaborators[].createdAt` | date |  |
| `collaborators[].email` | string |  |
| `collaborators[].firstName` | string |  |
| `collaborators[].id` | string |  |
| `collaborators[].lastName` | string |  |
| `collaborators[].permissions` | array<object> |  |
| `collaborators[].permissions[].action` | string |  |
| `collaborators[].permissions[].allowed` | boolean |  |
| `collaborators[].permissions[].message` | string |  |
| `collaborators[].role` | string |  |
| `collaborators[].userId` | string |  |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `startingToken` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/projects/:project_id/users` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-users.md) for the provider-specific parameters and requirements.

