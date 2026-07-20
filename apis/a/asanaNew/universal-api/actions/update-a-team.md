# Asana: Update a team

Updates a team in Asana.

```
PUT https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamGid": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamGid": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamGid` | string | yes |  |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "editTeamNameOrDescriptionAccessLevel": "Ava Chen",
      "editTeamVisibilityOrTrashTeamAccessLevel": "string",
      "endorsed": true,
      "gid": "string",
      "guestInviteManagementAccessLevel": "string",
      "joinRequestManagementAccessLevel": "string",
      "memberInviteManagementAccessLevel": "string",
      "name": "Ava Chen",
      "organization": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "permalinkUrl": "https://example.com",
      "resourceType": "string",
      "teamContentManagementAccessLevel": "string",
      "teamMemberRemovalAccessLevel": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editTeamNameOrDescriptionAccessLevel` | string |  |
| `editTeamVisibilityOrTrashTeamAccessLevel` | string |  |
| `endorsed` | boolean |  |
| `gid` | string |  |
| `guestInviteManagementAccessLevel` | string |  |
| `joinRequestManagementAccessLevel` | string |  |
| `memberInviteManagementAccessLevel` | string |  |
| `name` | string |  |
| `organization.gid` | string |  |
| `organization.name` | string |  |
| `organization.resourceType` | string |  |
| `permalinkUrl` | string |  |
| `resourceType` | string |  |
| `teamContentManagementAccessLevel` | string |  |
| `teamMemberRemovalAccessLevel` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Asana API, this operation is `PUT teams/:team_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-team.md) for the provider-specific parameters and requirements.

