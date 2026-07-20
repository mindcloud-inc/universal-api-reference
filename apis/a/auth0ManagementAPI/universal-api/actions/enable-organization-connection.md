# Auth0 Management: Enable Organization Connection

Enables a connection for an organization in Auth0 Management API.

```
POST https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/enable-organization-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/enable-organization-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/enable-organization-connection', {
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

```json
{
  "success": true,
  "data": [
    {
      "assign_membership_on_login": true,
      "connection_id": "string",
      "is_signup_enabled": true,
      "show_as_button": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assign_membership_on_login` | boolean |  |
| `connection_id` | string |  |
| `is_signup_enabled` | boolean |  |
| `show_as_button` | boolean |  |

## Native endpoint

Through the native Auth0 Management API, this operation is `POST /organizations/{id}/enabled_connections` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-organization-connection.md) for the provider-specific parameters and requirements.

