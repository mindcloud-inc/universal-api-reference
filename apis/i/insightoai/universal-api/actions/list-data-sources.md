# Insighto.ai: List Data Sources



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-data-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-data-sources?${params}`, {
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
      "attributes": {},
      "description": "string",
      "ds_status": "string",
      "ds_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "org_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `description` | string |  |
| `ds_status` | string |  |
| `ds_type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `org_id` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /datasource` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-data-sources.md) for the provider-specific parameters and requirements.

