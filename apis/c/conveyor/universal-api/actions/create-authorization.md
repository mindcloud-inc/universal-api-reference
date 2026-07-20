# Conveyor: Create Authorization

Creates an authorization in Conveyor from email or request.

```
POST https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-authorization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-authorization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email to authorize when not using a request id. |
| `requestId` | string | no | Authorization request id to approve. |
| `accessGroupIds[]` | array<string> | no | Access group identifiers for the authorization. |
| `ndaBypass` | boolean | no | Whether to bypass NDA for the authorization. |
| `expiresAt` | date | no | Authorization expiration date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Conveyor API returns.

## Native endpoint

Through the native Conveyor API, this operation is `POST /v2/exchange/authorizations` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-authorization.md) for the provider-specific parameters and requirements.

