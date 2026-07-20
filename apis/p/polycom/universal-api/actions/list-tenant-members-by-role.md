# Polycom: List Tenant Members By Role

Lists tenant members in Poly Lens for a selected role.

```
GET https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenant-members-by-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenant-members-by-role?connectionId=$CONNECTION_ID&query=query%20ListTenantMembersByRole(%24params%3A%20UserSearchParams!)%20%7B%20users(params%3A%20%24params)%20%7B%20edges%20%7B%20node%20%7B%20user_id%20email%20email_verified%20last_ip%20logins_count%20last_login%20%7D%20%7D%20%7D%20%7D&variables.params.grants%5B0%5D.resourceId=500c2d28-df9c-491a-84d7-a02ff4b2036d&variables.params.grants%5B0%5D.roles=admin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListTenantMembersByRole($params: UserSearchParams!) { users(params: $params) { edges { node { user_id email email_verified last_ip logins_count last_login } } } }",
  "variables.params.grants[0].resourceId": "500c2d28-df9c-491a-84d7-a02ff4b2036d",
  "variables.params.grants[0].roles": "admin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenant-members-by-role?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL document for the tenant-member search. Default: `query ListTenantMembersByRole($params: UserSearchParams!) { users(params: $params) { edges { node { user_id email email_verified last_ip logins_count last_login } } } }`. |
| `variables.params.grants[0].resourceId` | string | yes | The tenant to search for users. Example: `500c2d28-df9c-491a-84d7-a02ff4b2036d`. |
| `variables.params.grants[0].roles` | string | yes | Supported Poly Lens roles include admin, it-admin, user, and device_user. Default: `admin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "email_verified": true,
      "last_ip": "string",
      "last_login": "2026-05-07T12:00:00.000Z",
      "logins_count": 1,
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `email_verified` | boolean |  |
| `last_ip` | string |  |
| `last_login` | date |  |
| `logins_count` | number |  |
| `user_id` | string |  |

## Native endpoint

Through the native Polycom API, this operation is `POST /graphql` (base URL `https://api.silica-prod01.io.lens.poly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tenant-members-by-role.md) for the provider-specific parameters and requirements.

