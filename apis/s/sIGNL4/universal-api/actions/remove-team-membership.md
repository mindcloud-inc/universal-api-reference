# SIGNL4: Remove Team Membership

Deletes a team membership from SIGNL4.

```
DELETE https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/remove-team-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/remove-team-membership?connectionId=$CONNECTION_ID&teamId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/remove-team-membership?${params}`, {
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
| `teamId` | string | yes | ID of the team the user should be deleted from |
| `userId` | string | yes | ID of the user that should be deleted |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requesterUserId` | string | no | User ID of user which will remove the other user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SIGNL4 API returns.

## Native endpoint

Through the native SIGNL4 API, this operation is `DELETE /v2/teams/{teamId}/memberships/{userId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-team-membership.md) for the provider-specific parameters and requirements.

