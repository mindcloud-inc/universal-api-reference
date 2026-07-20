# Zendesk: List Organizations

Retrieves a list of organizations from Zendesk.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-organizations?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "details": "string",
      "domainNames": [
        "Ava Chen"
      ],
      "groupId": 1,
      "id": 1,
      "name": "Ava Chen",
      "sharedComments": true,
      "sharedTickets": true,
      "tags": [
        "string"
      ],
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
| `createdAt` | date | Creation timestamp. |
| `details` | string | Organization details. |
| `domainNames[]` | string | Organization domain names. |
| `groupId` | number | Default group id for the organization. |
| `id` | number | Organization id. |
| `name` | string | Organization name. |
| `sharedComments` | boolean | Whether comments are shared with organization members. |
| `sharedTickets` | boolean | Whether tickets are shared with organization members. |
| `tags[]` | string | Tags attached to the organization. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | URL of the organization resource. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /organizations.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

