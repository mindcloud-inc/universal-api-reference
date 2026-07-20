# Pabbly Hook: Filter Connections



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-connections?connectionId=$CONNECTION_ID&limit=25&offset=0&folderId=67592783069f7717b89ba992" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "folderId": "67592783069f7717b89ba992"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/filter-connections?${params}`, {
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
| `status` | string | no | Connection status selector. Example: `active`. |
| `folderId` | string | yes | Folder ID selector. Pabbly returns Invalid folder ID when this endpoint is run without a valid folder_id. Example: `67592783069f7717b89ba992`. |
| `name` | string | no | Connection name selector. Example: `Sample`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "connections": [
        {}
      ],
      "inactive": 1,
      "limit": 1,
      "page": 1,
      "total": 1,
      "totalConnections": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Active connection count. |
| `connections` | array<object> | Connections matching the filter. |
| `inactive` | number | Inactive connection count. |
| `limit` | number | Page size. |
| `page` | number | Current page number. |
| `total` | number | Total matching records. |
| `totalConnections` | number | Total connection count. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/connections` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/filter-connections.md) for the provider-specific parameters and requirements.

