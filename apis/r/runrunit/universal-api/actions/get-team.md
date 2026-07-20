# Runrun.it: Get Team

Retrieves a team from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-team?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-team?${params}`, {
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
| `id` | string | yes | Id path parameter. |

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
| `cost_center` | string | Cost center |
| `id` | number | Id of the team |
| `leader_id` | string | Id of the user team leader |
| `leader_name` | string | Name of the user team leader |
| `master_user_id` | string | [Deprecated] Use leader_id |
| `master_user_name` | string | [Deprecated] Use leader_name |
| `name` | string | Name of the team |
| `user_ids` | array<string> | Ids of team members |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /teams/:id` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

