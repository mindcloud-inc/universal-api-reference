# Auth0 Management: Add Organization Members

Adds members to an organization in Auth0 Management API.

```
POST https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/add-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/add-organization-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/add-organization-members', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Auth0 Management API returns.

## Native endpoint

Through the native Auth0 Management API, this operation is `POST /organizations/{id}/members` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-organization-members.md) for the provider-specific parameters and requirements.

