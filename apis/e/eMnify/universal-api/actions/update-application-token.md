# EMnify: Update Application Token

Updates an existing application token in EMnify.

```
PUT https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/update-application-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/update-application-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "Paste the auth_token from Retrieve Authentication Token",
  "applicationTokenId": "15701"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/update-application-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "Paste the auth_token from Retrieve Authentication Token",
    "applicationTokenId": "15701"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |
| `applicationTokenId` | number | yes | Application token ID to update. Example: `15701`. |
| `description` | string | no | Updated token description. Example: `Updated by Codex Stage 3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiryDate` | string | no | Updated expiry date. Example: `2026-03-27`. |
| `ip` | string | no | Updated IP/CIDR restriction. Example: `203.0.113.0/24`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EMnify API returns.

## Native endpoint

Through the native EMnify API, this operation is `PATCH /application_token/:application_token_id` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-application-token.md) for the provider-specific parameters and requirements.

