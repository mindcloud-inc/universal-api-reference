# Insighto.ai: List Data Source Files For Data Source Id



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-data-source-files-by-datasource-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-data-source-files-by-datasource-id?connectionId=$CONNECTION_ID&limit=25&offset=0&datasourceId=3c90c3cc-0d44-4b50-8888-8dd25736052a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "datasourceId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-data-source-files-by-datasource-id?${params}`, {
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
| `datasourceId` | string | yes | The UUID id of the datasource. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "description": "string",
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
| `ds_type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `org_id` | string |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `GET /datasource/:datasource_id/data_source_files` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-data-source-files-by-datasource-id.md) for the provider-specific parameters and requirements.

