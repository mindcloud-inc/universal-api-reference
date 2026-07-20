# Asana: Add a user to a team

Adds a user to a team in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-user-to-a-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-user-to-a-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataUser": "string",
  "teamGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-user-to-a-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataUser": "string",
    "teamGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataUser` | string | yes |  |
| `teamGid` | string | yes | Asana team gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |
| `data.user` | string | no | Asana user parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "isAdmin": true,
      "isGuest": true,
      "isLimitedAccess": true,
      "resourceType": "string",
      "team": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "user": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `isAdmin` | boolean |  |
| `isGuest` | boolean |  |
| `isLimitedAccess` | boolean |  |
| `resourceType` | string |  |
| `team.gid` | string |  |
| `team.name` | string |  |
| `team.resourceType` | string |  |
| `user.gid` | string |  |
| `user.name` | string |  |
| `user.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST teams/:team_gid/addUser` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-user-to-a-team.md) for the provider-specific parameters and requirements.

