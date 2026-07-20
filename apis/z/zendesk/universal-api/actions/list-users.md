# Zendesk: List Users

Retrieves a list of users from Zendesk.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-users?${params}`, {
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
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "lastLoginAt": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "name": "Ava Chen",
      "organizationId": 1,
      "role": "string",
      "timeZone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | number |  |
| `lastLoginAt` | date |  |
| `locale` | string |  |
| `name` | string |  |
| `organizationId` | number |  |
| `role` | string |  |
| `timeZone` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Zendesk API, this operation is `GET /users.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

