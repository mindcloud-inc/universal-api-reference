# Zendesk: Create Organization Membership

Creates a new organization membership in Zendesk.

```
POST https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-organization-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-organization-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organization_membership.user_id": 1,
  "organization_membership.organization_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-organization-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organization_membership.user_id": 1,
    "organization_membership.organization_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organization_membership.user_id` | number | yes | Organization membership user ID |
| `organization_membership.organization_id` | number | yes | Organization membership organization ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "id": 1,
      "organizationId": 1,
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
| `default` | boolean | Whether this is the user's default organization. |
| `id` | number | Organization membership id. |
| `organizationId` | number | Organization id for the membership. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the organization membership resource. |
| `userId` | number | User id for the membership. |

## Native endpoint

Through the native Zendesk API, this operation is `POST /organization_memberships.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-membership.md) for the provider-specific parameters and requirements.

