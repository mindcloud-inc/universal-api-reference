# Xano: Search Table Records

Finds records in a Xano table by search filters.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/search-table-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/search-table-records?connectionId=$CONNECTION_ID&table_id=1&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "table_id": "1",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/search-table-records?${params}`, {
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
| `table_id` | number | yes |  |
| `workspace_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "curPage": 1,
      "items": [
        {
          "createdAt": 1,
          "id": 1
        }
      ],
      "itemsReceived": 1,
      "itemsTotal": 1,
      "offset": 1,
      "pageTotal": 1,
      "perPage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `curPage` | number |  |
| `items[].createdAt` | number |  |
| `items[].id` | number |  |
| `itemsReceived` | number |  |
| `itemsTotal` | number |  |
| `offset` | number |  |
| `pageTotal` | number |  |
| `perPage` | number |  |

## Native endpoint

Through the native Xano API, this operation is `POST /api%3Ameta/workspace/:workspace_id/table/:table_id/content/search` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-table-records.md) for the provider-specific parameters and requirements.

