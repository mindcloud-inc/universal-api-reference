# Notion: Update Data Source



```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-data-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-data-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataSourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSourceId` | string | yes | ID of a Notion data source. |
| `title[]` | array<object> | no | Title of the data source as it appears in Notion. |
| `icon` | object | no | Page icon for the data source. |
| `properties` | object | no | The property schema of the data source. Keys are property names or IDs, and null values remove properties. |
| `inTrash` | boolean | no | Whether the data source should be moved to or from the trash. |
| `parent` | object | no | The parent database to move the data source to. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Notion API returns.

## Native endpoint

Through the native Notion API, this operation is `PATCH /data_sources/:data_source_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-source.md) for the provider-specific parameters and requirements.

