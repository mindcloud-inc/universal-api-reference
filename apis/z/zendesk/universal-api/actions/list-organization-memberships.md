# Zendesk: List Organization Memberships

Retrieves a list of organization memberships from Zendesk.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-organization-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-organization-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-organization-memberships?${params}`, {
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
| `organization_id` | number | no | Filter memberships by organization ID. |

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

Through the native Zendesk API, this operation is `GET /organization_memberships.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-memberships.md) for the provider-specific parameters and requirements.

