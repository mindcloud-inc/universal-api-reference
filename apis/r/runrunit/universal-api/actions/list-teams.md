# Runrun.it: List Teams

Retrieves teams from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-teams?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sort by column |
| `sortDir` | string | no | Sort direction ('asc' or 'desc') |
| `searchTerm` | string | no | Filter by term |
| `filterId` | number | no | Filter by an existing filter |

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

Through the native Runrun.it API, this operation is `GET /teams` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

