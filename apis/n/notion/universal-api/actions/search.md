# Notion: Search

Finds pages and data sources in Notion by title.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/search?${params}`, {
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
| `query` | string | no | Text to search for in titles and content. Example: `project roadmap`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterProperty` | list | no | Property type to filter by. One of: `0`. Example: `object`. |
| `filterValue` | list | no | Object value to filter search results. One of: `0`, `1`. Example: `data_source`. |
| `sortDirection` | list | no | Sort direction for result ordering. One of: `0`, `1`. Example: `ascending`. |
| `sortTimestamp` | list | no | Timestamp field used for sorting. One of: `0`. Example: `last_edited_time`. |
| `pageSize` | number | no | Number of results to return (max 100). Default: `100`. Example: `100`. |
| `startCursor` | string | no | Pagination cursor returned by previous response. Example: `d7f7f7f7-7f7f-7f7f-7f7f-d7f7f7f7f7f7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdBy": {},
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inTrash": true,
      "isLocked": true,
      "lastEditedBy": {},
      "lastEditedTime": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "parent": {},
      "properties": {},
      "publicUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdBy` | object |  |
| `createdTime` | date |  |
| `id` | string |  |
| `inTrash` | boolean |  |
| `isLocked` | boolean |  |
| `lastEditedBy` | object |  |
| `lastEditedTime` | date |  |
| `object` | string |  |
| `parent` | object |  |
| `properties` | object |  |
| `publicUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Notion API, this operation is `POST /search` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

