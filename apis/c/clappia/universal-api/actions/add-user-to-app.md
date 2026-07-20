# Clappia: Add User to App

Creates a new app user membership in Clappia.

```
POST https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-user-to-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-user-to-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "permissions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/add-user-to-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "permissions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | no | Email address of the app user to add. |
| `phoneNumber` | string | no | Phone number of the app user to add. |
| `appId` | string | yes | Clappia app ID. |
| `permissions` | object | yes | Permissions object describing the app access to grant. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /app/addUserToApp` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-app.md) for the provider-specific parameters and requirements.

