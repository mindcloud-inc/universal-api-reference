# Bridge: Create User Management Session

Creates a user management session in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-user-management-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-user-management-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userAccessToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-user-management-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userAccessToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userAccessToken` | string | yes | Bridge user access token returned by the Authorization token action. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional callback URL for redirecting the user at the exit of the user management session |
| `context` | string | no | Optional context string to append to the callback URL when exiting the user management session. It can contain up to 100 alphanumeric characters, including the hyphen (-). |
| `accountTypes` | string | no | Minimum account types required. We suggest `payment` to ensure the best user experience Default: `payment`. |
| `userEmail` | string | no | Mandatory, except in the case of temporary bank synchronization |
| `countryCode` | string | no | On the displayed providers list, the country selector will default to the country parameter if provided. If you customize the highlighted banks on the dashboard, this parameter will be disabled. |
| `capabilities[]` | array<string> | no | Filter the provider capabilities you need. When multiple values are specified, they are combined using an `AND` operation |
| `allowAccountSelection` | boolean | no | Allow or disallow the selection of the accounts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | User management session identifier |
| `url` | string | User management session web funnel URL |

## Native endpoint

Through the native Bridge API, this operation is `POST /aggregation/user-management-sessions` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-management-session.md) for the provider-specific parameters and requirements.

