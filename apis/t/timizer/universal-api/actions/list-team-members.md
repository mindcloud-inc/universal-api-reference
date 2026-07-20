# Timizer: List Team Members

Retrieves team members from Timizer.

```
GET https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-team-members?${params}`, {
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
| `teamId` | string | no | ID of the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isActive": true,
      "isExternalUser": true,
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "lastLoginAt": "2026-05-07T12:00:00.000Z",
      "role": "string",
      "teamId": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isActive` | boolean |  |
| `isExternalUser` | boolean |  |
| `joinedAt` | date |  |
| `lastLoginAt` | date |  |
| `role` | string |  |
| `teamId` | number |  |
| `user` | object |  |

## Native endpoint

Through the native Timizer API, this operation is `GET /app/admin-teams/:teamId/members` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

