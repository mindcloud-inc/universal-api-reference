# Sales Cookie: Create Or Update Team

Creates or updates a team in Sales Cookie by name.

```
PUT https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-or-update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-or-update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-or-update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Team name used to create or update the team. |
| `description` | string | no |  |
| `managerId` | string | no | Optional system user ID for the team manager. |
| `parentTeamId` | string | no | Optional parent team ID. |
| `managerCanViewResults` | boolean | no |  |
| `managerCanViewCredits` | boolean | no |  |
| `membersCanViewCredits` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "managerId": "string",
      "name": "Ava Chen",
      "parentTeamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `managerId` | string |  |
| `name` | string |  |
| `parentTeamId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `POST /Api/SetTeam` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-team.md) for the provider-specific parameters and requirements.

