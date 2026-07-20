# RICOH360 Tours: Invite Team Member



```
POST https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/invite-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RICOH360 Tours `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/invite-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "memberRole": "0",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/invite-team-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "memberRole": "0",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the invited team member. |
| `memberRole` | string | yes | Team member role enum, for example LIMITED or AGENT. One of: `0`, `1`, `2`, `3`. |
| `teamId` | string | yes | Team ID to invite the member into. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RICOH360 Tours API returns.

## Native endpoint

Through the native RICOH360 Tours API, this operation is `POST /graphql` (base URL `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-team-member.md) for the provider-specific parameters and requirements.

