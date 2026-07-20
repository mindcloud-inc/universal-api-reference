# Webshipper: List Reports

Retrieves reports from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-reports?${params}`, {
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
      "created_at": "string",
      "csv_download_url": "https://example.com",
      "end_time": "string",
      "error_message": "string",
      "failed": true,
      "id": "string",
      "json_download_url": "https://example.com",
      "order_ids": "string",
      "output_formats": "string",
      "parameters": "string",
      "pdf_download_url": "https://example.com",
      "start_time": "string",
      "type": "string",
      "updated_at": "string",
      "xlsx_download_url": "https://example.com",
      "xml_download_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `csv_download_url` | string |  |
| `end_time` | string |  |
| `error_message` | string |  |
| `failed` | boolean |  |
| `id` | string |  |
| `json_download_url` | string |  |
| `order_ids` | string |  |
| `output_formats` | string |  |
| `parameters` | string |  |
| `pdf_download_url` | string |  |
| `start_time` | string |  |
| `type` | string |  |
| `updated_at` | string |  |
| `xlsx_download_url` | string |  |
| `xml_download_url` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /reports` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

