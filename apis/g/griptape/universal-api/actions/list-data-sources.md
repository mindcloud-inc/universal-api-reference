# Griptape: List Data Sources

Finds data sources in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-data-sources?${params}`, {
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
      "data_connectors": [
        {
          "bucket_id": "string",
          "config": {
            "webscraper": {
              "urls": [
                "https://example.com"
              ]
            }
          },
          "created_at": "string",
          "created_by": "string",
          "data_connector_id": "string",
          "description": "string",
          "name": "Ava Chen",
          "organization_id": "string",
          "schedule_expression": "string",
          "transforms": [
            "string"
          ],
          "type": "string",
          "updated_at": "string"
        }
      ],
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_connectors[].bucket_id` | string |  |
| `data_connectors[].config.webscraper.urls` | array<string> |  |
| `data_connectors[].created_at` | string |  |
| `data_connectors[].created_by` | string |  |
| `data_connectors[].data_connector_id` | string |  |
| `data_connectors[].description` | string |  |
| `data_connectors[].name` | string |  |
| `data_connectors[].organization_id` | string |  |
| `data_connectors[].schedule_expression` | string |  |
| `data_connectors[].transforms` | array |  |
| `data_connectors[].type` | string |  |
| `data_connectors[].updated_at` | string |  |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/data-connectors` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-sources.md) for the provider-specific parameters and requirements.

