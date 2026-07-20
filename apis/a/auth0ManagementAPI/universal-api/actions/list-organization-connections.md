# Auth0 Management: List Organization Connections

Retrieves enabled connections for an organization in Auth0 Management API.

```
GET https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/list-organization-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/list-organization-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/list-organization-connections?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Auth0 Management API, this operation is `GET /organizations/{id}/enabled_connections` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-connections.md) for the provider-specific parameters and requirements.

