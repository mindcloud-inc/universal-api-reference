# Files.com: Get Site Usage

Retrieves site usage data from Files.com.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site-usage?${params}`, {
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
      "bytes_sent": 1,
      "current_storage": 1,
      "end_at": "2026-05-07T12:00:00.000Z",
      "high_water_storage": 1,
      "high_water_user_count": 1,
      "id": 1,
      "start_at": "2026-05-07T12:00:00.000Z",
      "total_billable_transfer_usage": 1,
      "total_billable_usage": 1,
      "usage_by_top_level_dir": [
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
| `bytes_sent` | number |  |
| `current_storage` | number |  |
| `end_at` | date |  |
| `high_water_storage` | number |  |
| `high_water_user_count` | number |  |
| `id` | number |  |
| `start_at` | date |  |
| `total_billable_transfer_usage` | number |  |
| `total_billable_usage` | number |  |
| `usage_by_top_level_dir` | array<object> |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /site/usage` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-usage.md) for the provider-specific parameters and requirements.

