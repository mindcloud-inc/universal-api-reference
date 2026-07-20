# Onfleet: Update Team

Updates an existing team in Onfleet.

```
PUT https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | The Onfleet team ID. |
| `name` | string | no | A unique name for the team. |
| `workers[]` | array<string> | no | An array of worker IDs. |
| `managers[]` | array<string> | no | An array of managing administrator IDs. |
| `hub` | string | no | Optional. The ID of the team's hub. |
| `enableSelfAssignment` | boolean | no | Whether team self-assignment is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enableSelfAssignment": true,
      "id": "string",
      "managers": [
        "string"
      ],
      "name": "Ava Chen",
      "tasks": [
        "string"
      ],
      "workers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enableSelfAssignment` | boolean |  |
| `id` | string |  |
| `managers` | array<string> |  |
| `name` | string |  |
| `tasks` | array |  |
| `workers` | array<string> |  |

## Native endpoint

Through the native Onfleet API, this operation is `PUT /teams/:teamId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

