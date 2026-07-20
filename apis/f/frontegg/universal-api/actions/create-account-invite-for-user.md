# Frontegg: Create Account Invite For User

Creates an account invitation for a user in Frontegg.

```
POST https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-account-invite-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-account-invite-for-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "expiresInMinutes": 1,
  "shouldSendEmail": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-account-invite-for-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "expiresInMinutes": 1,
    "shouldSendEmail": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiresInMinutes` | number | yes | Invitation expiration time in minutes. |
| `shouldSendEmail` | boolean | yes | Whether to send the invitation email. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frontegg API returns.

## Native endpoint

Through the native Frontegg API, this operation is `POST /identity/resources/tenants/invites/v1/user` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-invite-for-user.md) for the provider-specific parameters and requirements.

