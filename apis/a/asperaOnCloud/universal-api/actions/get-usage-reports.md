# Aspera on Cloud: List Usage Reports

Retrieves usage reports from Aspera on Cloud.

```
GET https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-usage-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-usage-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/get-usage-reports?${params}`, {
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
      "node_id": "string",
      "reporting_period_bytes": 1,
      "reporting_period_bytes_in": 1,
      "reporting_period_bytes_out": 1,
      "total_bytes": 1,
      "total_bytes_in": 1,
      "total_bytes_out": 1,
      "updated_at": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `node_id` | string |  |
| `reporting_period_bytes` | number |  |
| `reporting_period_bytes_in` | number |  |
| `reporting_period_bytes_out` | number |  |
| `total_bytes` | number |  |
| `total_bytes_in` | number |  |
| `total_bytes_out` | number |  |
| `updated_at` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Aspera on Cloud API, this operation is `GET /v1/usage_reports` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-reports.md) for the provider-specific parameters and requirements.

