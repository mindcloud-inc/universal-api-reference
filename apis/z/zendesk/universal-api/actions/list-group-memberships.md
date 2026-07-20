# Zendesk: List Group Memberships

Retrieves a list of group memberships from Zendesk.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-group-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-group-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-group-memberships?${params}`, {
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
| `user_id` | number | no | Filter memberships by user ID. |
| `group_id` | number | no | Filter memberships by group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "groupId": 1,
      "id": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `default` | boolean | Whether this is the user's default group. |
| `groupId` | number | Group id for the membership. |
| `id` | number | Group membership id. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the group membership resource. |
| `userId` | number | User id for the membership. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /group_memberships.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-memberships.md) for the provider-specific parameters and requirements.

