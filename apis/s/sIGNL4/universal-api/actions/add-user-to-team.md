# SIGNL4: Add User To Team

Creates a team membership in SIGNL4.

```
POST https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/add-user-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/add-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/add-user-to-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Id of team the user should be invited to. |
| `userId` | string | yes | Id of user you want to add to a team. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roleId` | string | no |  |
| `setUserOnDuty` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mailAddress": "string",
      "memberSince": "2026-05-07T12:00:00.000Z",
      "roleId": "string",
      "status": 1,
      "teamId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mailAddress` | string |  |
| `memberSince` | date |  |
| `roleId` | string |  |
| `status` | number |  |
| `teamId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `POST /v2/teams/{teamId}/memberships/{userId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-team.md) for the provider-specific parameters and requirements.

