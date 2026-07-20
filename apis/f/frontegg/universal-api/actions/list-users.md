# Frontegg: List Users

Finds users in your Frontegg environment.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-users?${params}`, {
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
| `limit` | number | no | Maximum number of users to return (default 50, maximum 200). |
| `offset` | number | no | Page number to retrieve, starting at 0. |
| `email` | string | no | Filter users by email. |
| `tenantId` | string | no | Filter users by tenant ID. |
| `sortBy` | string | no | Sort by createdAt, name, email, id, verified, isLocked, provider, or tenantId. |
| `order` | string | no | Sort order: ASC or DESC. |
| `namePrefix` | string | no | Filter users by name prefix. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | no | Filter by identifier prefix. Must be used with Identifier Type. |
| `identifierType` | string | no | Identifier type: email, phoneNumber, or username. |
| `includeSubTenants` | boolean | no | Include sub-tenants when searching users. |
| `ids` | string | no | Specific user IDs to retrieve. |
| `externalIds` | string | no | Filter users by external IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedForTenant": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "isLocked": true,
      "managedBy": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "profilePictureUrl": "https://example.com",
      "provider": "string",
      "sub": "string",
      "tenantId": "string",
      "tenantIds": [
        "string"
      ],
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedForTenant` | boolean |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `managedBy` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `profilePictureUrl` | string |  |
| `provider` | string |  |
| `sub` | string |  |
| `tenantId` | string |  |
| `tenantIds` | array<string> |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/users/v3` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

