# Zendesk: Search Users

Finds users in Zendesk by search query.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/search-users?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/search-users?${params}`, {
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
| `query` | string | yes | Search query string. Supports Zendesk user search syntax. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "organizationId": 1,
      "role": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the user is active. |
| `createdAt` | date | Creation timestamp. |
| `email` | string | User email. |
| `id` | number | User id. |
| `name` | string | User name. |
| `organizationId` | number | Organization id attached to the user. |
| `role` | string | User role. |
| `tags[]` | string | Tags attached to the user. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the user resource. |
| `verified` | boolean | Whether the user is verified. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /users/search.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.

