# Conveyor: List Connections

Retrieves connections from Conveyor with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-connections?${params}`, {
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
| `domain` | string | no | Filter by bare domain, for example example.com. Do not include https:// or www. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connections": [
        {
          "_type": "string",
          "authorizations_count": 1,
          "authorizations_removed_count": 1,
          "authorizations_with_access_count": 1,
          "created_at": "2026-05-07T12:00:00.000Z",
          "crm_id": "string",
          "crm_link": "https://example.com",
          "domain": "string",
          "id": "string",
          "latest_activity_at": "2026-05-07T12:00:00.000Z",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "page": 1,
      "per_page": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connections` | array<object> | Conveyor connection records. |
| `connections[]._type` | string | Conveyor connection resource type. |
| `connections[].authorizations_count` | number | Total authorizations count. |
| `connections[].authorizations_removed_count` | number | Removed authorizations count. |
| `connections[].authorizations_with_access_count` | number | Authorizations with access count. |
| `connections[].created_at` | date | Connection creation timestamp. |
| `connections[].crm_id` | string | Linked CRM record ID. |
| `connections[].crm_link` | string | Linked CRM record URL. |
| `connections[].domain` | string | Connection domain. |
| `connections[].id` | string | Connection UUID. |
| `connections[].latest_activity_at` | date | Latest activity timestamp. |
| `connections[].updated_at` | date | Connection update timestamp. |
| `page` | number | Current page number. |
| `per_page` | number | Page size. |
| `total_pages` | number | Total pages. |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/exchange/connections` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-connections.md) for the provider-specific parameters and requirements.

