# Faithlife: Invite Users To Group

Creates invites for a group in Faithlife.

```
POST https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/invite-users-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faithlife `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/invite-users-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/invite-users-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The Faithlife group ID or token to invite users into. |
| `invites[0].accountId` | string | no | Optional Faithlife account ID to invite. |
| `invites[0].emailInvite.email` | string | no | Optional email address to invite when no account ID is provided. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Faithlife API returns.

## Native endpoint

Through the native Faithlife API, this operation is `POST /groups/:groupId/invites` (base URL `https://accountsapi.logos.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-users-to-group.md) for the provider-specific parameters and requirements.

