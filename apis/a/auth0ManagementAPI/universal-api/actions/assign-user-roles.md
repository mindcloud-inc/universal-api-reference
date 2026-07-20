# Auth0 Management: Assign User Roles

Assigns roles to a user in Auth0 Management API.

```
PUT https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/assign-user-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/assign-user-roles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/assign-user-roles', {
  method: 'PUT',
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Auth0 Management API returns.

## Native endpoint

Through the native Auth0 Management API, this operation is `POST /users/{id}/roles` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-user-roles.md) for the provider-specific parameters and requirements.

