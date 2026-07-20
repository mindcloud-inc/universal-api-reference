# SeekTable: Remove Users From Team Group

Removes users from a SeekTable team group.

```
DELETE https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/remove-users-from-team-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/remove-users-from-team-group?connectionId=$CONNECTION_ID&id=1&groupId=group1guid&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "groupId": "group1guid",
  "emails[]": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/remove-users-from-team-group?${params}`, {
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
| `id` | number | yes | ID of the user account that owns the team. Example: `1`. |
| `groupId` | string | yes | ID of the team group. Example: `group1guid`. |
| `emails[]` | array<string> | yes | Login emails to remove from the specified team group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `DELETE /api/account/:id/team/group/:group_id/member` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-users-from-team-group.md) for the provider-specific parameters and requirements.

