# ActiveTrail: Remove Member from Group

Removes a member from a group in ActiveTrail.

```
DELETE https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/remove-member-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/remove-member-from-group?connectionId=$CONNECTION_ID&id=1&memberId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "memberId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/remove-member-from-group?${params}`, {
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
| `id` | number | yes | Group id. Can be found using the account groups endpoint or in the UI. |
| `memberId` | number | yes | The member contact id to remove from the group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `DELETE /groups/:id/members/:memberId` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-member-from-group.md) for the provider-specific parameters and requirements.

