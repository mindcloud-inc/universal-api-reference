# Notion: List Data Source Templates

Retrieves page templates for a Notion data source.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-data-source-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-data-source-templates?connectionId=$CONNECTION_ID&limit=25&offset=0&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/list-data-source-templates?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Filter templates by name. |
| `startCursor` | string | no | Cursor for pagination. |
| `pageSize` | number | no | Maximum number of templates per page (max 100). Default: `100`. |

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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more templates are available. |
| `nextCursor` | string | Cursor for next page. |
| `object` | string | List wrapper type. |
| `results` | array<object> | Template results. |

## Native endpoint

Through the native Notion API, this operation is `GET /data_sources/:data_source_id/templates` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-data-source-templates.md) for the provider-specific parameters and requirements.

