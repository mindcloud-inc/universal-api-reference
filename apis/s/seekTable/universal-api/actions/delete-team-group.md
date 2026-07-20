# SeekTable: Delete Team Group

Deletes an existing team group from SeekTable.

```
DELETE https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/delete-team-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/delete-team-group?connectionId=$CONNECTION_ID&id=1&groupId=group1guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "groupId": "group1guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/delete-team-group?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `DELETE /api/account/:id/team/group/:group_id` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-team-group.md) for the provider-specific parameters and requirements.

