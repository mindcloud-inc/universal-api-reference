# Runrun.it: Add User To Team

Adds a user to a team in Runrun.it.

```
PUT https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/add-user-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/add-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/add-user-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Id path parameter. |
| `userId` | string | yes | New team member id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamPartnership` | boolean | no | Flag to make the new team member and other members, partners |

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

Through the native Runrun.it API, this operation is `POST /teams/:id/add_member` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-team.md) for the provider-specific parameters and requirements.

