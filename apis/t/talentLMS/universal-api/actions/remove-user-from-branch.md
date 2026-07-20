# TalentLMS: Remove User from Branch

Removes a user from a branch in TalentLMS.

```
DELETE https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/remove-user-from-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/remove-user-from-branch?connectionId=$CONNECTION_ID&branchId=1&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branchId": "1",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/remove-user-from-branch?${params}`, {
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
| `branchId` | number | yes | Numeric branch ID. |
| `userId` | number | yes | Numeric user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TalentLMS API returns.

## Native endpoint

Through the native TalentLMS API, this operation is `DELETE /branch-users` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-branch.md) for the provider-specific parameters and requirements.

