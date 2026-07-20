# Productlane: Invite User

Invites a user to your Productlane workspace.

```
POST https://connect.mindcloud.co/v1/universal/productlane/latest/actions/invite-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/invite-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps+productlane-stage3@mindcloud.co",
  "name": "Apps Stage 3",
  "role": "VIEWER"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/invite-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps+productlane-stage3@mindcloud.co",
    "name": "Apps Stage 3",
    "role": "VIEWER"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to invite. Example: `apps+productlane-stage3@mindcloud.co`. |
| `name` | string | yes | Display name for the invited user. Example: `Apps Stage 3`. |
| `role` | string | yes | Initial role for the invited user. Example: `VIEWER`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `POST /users/invite` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user.md) for the provider-specific parameters and requirements.

