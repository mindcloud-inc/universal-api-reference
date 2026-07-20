# Notion: Query Data Source

Retrieves filtered records from a Notion data source.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/query-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/query-data-source?connectionId=$CONNECTION_ID&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/query-data-source?${params}`, {
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
| `dataSourceId` | string | yes | ID of the data source. |
| `filter` | object | no | Filter conditions for the query body. |
| `resultType` | string | no | Limit results to a specific object type. |
| `sorts` | list<object> | no | Sort definitions for query results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterProperties` | list<string> | no | Property IDs used to limit filter formula computation. |
| `startCursor` | string | no | Cursor for pagination. |
| `pageSize` | number | no | Maximum number of results per page (max 100). Default: `100`. |
| `archived` | boolean | no | Include archived pages in query results. |
| `inTrash` | boolean | no | Include pages currently in trash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "nextCursor": "string",
      "object": "string",
      "results": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more results are available. |
| `nextCursor` | string | Cursor for next page. |
| `object` | string | List wrapper type. |
| `results` | array<object> | Queried page results. |
| `type` | string | Result container type. |

## Native endpoint

Through the native Notion API, this operation is `POST /data_sources/:data_source_id/query` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-data-source.md) for the provider-specific parameters and requirements.

