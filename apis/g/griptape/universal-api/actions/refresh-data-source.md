# Griptape: Refresh Data Source

Creates a data source refresh job in Griptape.

```
POST https://connect.mindcloud.co/v1/universal/griptape/latest/actions/refresh-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/refresh-data-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataSourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/refresh-data-source', {
  method: 'POST',
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
| `dataSourceId` | string | yes | The data source ID to refresh. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes_ingested": 1,
      "completed_at": "string",
      "created_at": "string",
      "created_by": "string",
      "data_connector_id": "string",
      "data_job_id": "string",
      "status": "string",
      "status_detail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes_ingested` | number |  |
| `completed_at` | string |  |
| `created_at` | string |  |
| `created_by` | string |  |
| `data_connector_id` | string |  |
| `data_job_id` | string |  |
| `status` | string |  |
| `status_detail` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `POST /api/data-connectors/:data_source_id/data-jobs` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-data-source.md) for the provider-specific parameters and requirements.

