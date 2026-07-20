# Codemagic: Create Team Variable Group

Creates a new variable group for a Codemagic team.

```
POST https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/create-team-variable-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/create-team-variable-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "name": "Ava Chen",
  "advancedSecurity": {
    "enabled": false,
    "selected_apps": []
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/create-team-variable-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "name": "Ava Chen",
    "advancedSecurity": {"enabled":false,"selected_apps":[]}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Codemagic team identifier. |
| `name` | string | yes | Variable group name. Codemagic disallows periods and dollar signs. |
| `advancedSecurity` | object | yes | Advanced security object with enabled and selected_apps fields. Default: `{"enabled":false,"selected_apps":[]}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `POST /api/v3/teams/:team_id/variable-groups` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-variable-group.md) for the provider-specific parameters and requirements.

