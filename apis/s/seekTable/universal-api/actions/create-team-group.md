# SeekTable: Create Team Group

Creates a new team group in SeekTable.

```
POST https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/create-team-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/create-team-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "name": "Codex Stage 3 Group"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/create-team-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "name": "Codex Stage 3 Group"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the user account that owns the team. Example: `1`. |
| `name` | string | yes | Name of the new team group. Example: `Codex Stage 3 Group`. |
| `reportOverrideParameters` | object | no | Optional key-value map of report parameter overrides for this team group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `POST /api/account/:id/team/group` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-group.md) for the provider-specific parameters and requirements.

