# Zendesk: Create Group Membership

Creates a new group membership in Zendesk.

```
POST https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-group-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_membership.user_id": 1,
  "group_membership.group_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-group-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_membership.user_id": 1,
    "group_membership.group_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group_membership.user_id` | number | yes | Group membership user ID |
| `group_membership.group_id` | number | yes | Group membership group ID |

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

Through the native Zendesk API, this operation is `POST /group_memberships.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-membership.md) for the provider-specific parameters and requirements.

