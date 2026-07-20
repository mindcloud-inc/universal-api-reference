# Notion: Retrieve Data Source

Retrieves a data source from Notion.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-data-source?connectionId=$CONNECTION_ID&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-data-source?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastEditedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | Creation timestamp. |
| `id` | string | Data source identifier. |
| `lastEditedTime` | date | Last edit timestamp. |
| `name` | string | Data source name. |
| `object` | string | Returned object type. |
| `url` | string | Data source URL. |

## Native endpoint

Through the native Notion API, this operation is `GET /data_sources/:data_source_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-data-source.md) for the provider-specific parameters and requirements.

