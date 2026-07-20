# Ecotrak: Create User

Creates a new user in Ecotrak.

```
POST https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecotrak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "jobTitleId": 1,
  "ssoUser": true,
  "timezone": "string",
  "nteLimit": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "jobTitleId": 1,
    "ssoUser": true,
    "timezone": "string",
    "nteLimit": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Ecotrak company ID. |
| `email` | string | yes | User email address. |
| `firstName` | string | yes | User first name. |
| `lastName` | string | yes | User last name. |
| `jobTitleId` | number | yes | Ecotrak job title ID. |
| `ssoUser` | boolean | yes | Whether the user authenticates via SSO. |
| `password` | string | no | Password for non-SSO users. |
| `timezone` | string | yes | User timezone. |
| `nteLimit` | number | yes | Maximum not-to-exceed limit. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecotrak API returns.

## Native endpoint

Through the native Ecotrak API, this operation is `POST /v2/user` (base URL `https://api.ecotrak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

