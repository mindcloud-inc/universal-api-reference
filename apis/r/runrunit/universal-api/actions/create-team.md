# Runrun.it: Create Team

Creates a new team in Runrun.it.

```
POST https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "team.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `team.name` | string | yes | Name of the team |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `team.masterUserId` | string | no | [Deprecated] Use leader_id |
| `team.costCenter` | string | no | Cost center |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost_center": "string",
      "id": 1,
      "leader_id": "string",
      "leader_name": "Ava Chen",
      "master_user_id": "string",
      "master_user_name": "Ava Chen",
      "name": "Ava Chen",
      "user_ids": [
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
| `cost_center` | string |  |
| `id` | number |  |
| `leader_id` | string |  |
| `leader_name` | string |  |
| `master_user_id` | string |  |
| `master_user_name` | string |  |
| `name` | string |  |
| `user_ids` | array<string> |  |

## Native endpoint

Through the native Runrun.it API, this operation is `POST /teams` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

