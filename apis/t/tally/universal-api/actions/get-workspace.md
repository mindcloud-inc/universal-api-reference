# Tally: Get Workspace



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdByUserId": "string",
      "id": "string",
      "index": 1,
      "members": [
        {
          "authenticationMethodsCount": 1,
          "avatarUrl": "https://example.com",
          "createdAt": "string",
          "email": "ava@example.com",
          "emailDomain": {},
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "hasPasswordSet": true,
          "hasTwoFactorEnabled": true,
          "id": "string",
          "isBlocked": true,
          "isDeleted": true,
          "lastName": "Chen",
          "organizationId": "string",
          "ssoIsConnectedWithApple": true,
          "ssoIsConnectedWithGoogle": true,
          "timezone": "string",
          "updatedAt": "string"
        }
      ],
      "name": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `createdByUserId` | string |  |
| `id` | string |  |
| `index` | number |  |
| `members[].authenticationMethodsCount` | number |  |
| `members[].avatarUrl` | string |  |
| `members[].createdAt` | string |  |
| `members[].email` | string |  |
| `members[].emailDomain` | object |  |
| `members[].firstName` | string |  |
| `members[].fullName` | string |  |
| `members[].hasPasswordSet` | boolean |  |
| `members[].hasTwoFactorEnabled` | boolean |  |
| `members[].id` | string |  |
| `members[].isBlocked` | boolean |  |
| `members[].isDeleted` | boolean |  |
| `members[].lastName` | string |  |
| `members[].organizationId` | string |  |
| `members[].ssoIsConnectedWithApple` | boolean |  |
| `members[].ssoIsConnectedWithGoogle` | boolean |  |
| `members[].timezone` | string |  |
| `members[].updatedAt` | string |  |
| `name` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET workspaces/:workspaceId` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

