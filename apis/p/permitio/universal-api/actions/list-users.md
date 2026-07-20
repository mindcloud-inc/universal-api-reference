# Permit.io: List Users



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0&projId=string&envId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projId": "string",
  "envId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/list-users?${params}`, {
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
| `projId` | string | yes | Permit project identifier or key. |
| `envId` | string | yes | Permit environment identifier or key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associatedTenants": [
        {}
      ],
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "environmentId": "string",
      "firstName": "Ava",
      "id": "string",
      "key": "string",
      "lastName": "Chen",
      "organizationId": "string",
      "projectId": "string",
      "roles": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatedTenants` | array<object> |  |
| `attributes` | object |  |
| `createdAt` | date |  |
| `email` | string |  |
| `environmentId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `key` | string |  |
| `lastName` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `roles` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/facts/:projId/:envId/users` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

