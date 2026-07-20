# Webshipper: Create Report

Creates a report in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.type": "reports",
  "data.relationships.reportType.data.type": "report_types"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.type": "reports",
    "data.relationships.reportType.data.type": "report_types"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes.endTime` | string | no | Report end time in ISO-8601 format. |
| `data.attributes.outputFormats` | string | no | Output formats to generate. |
| `data.attributes.startTime` | string | no | Report start time in ISO-8601 format. |
| `data.relationships.reportType.data.id` | string | no | Report type ID. |
| `data.type` | string | yes | Use the default value `reports`. Default: `reports`. |
| `data.relationships.reportType.data.type` | string | yes | Use the default value `report_types`. Default: `report_types`. |

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
      "failed": "string",
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
| `failed` | string |  |
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

Through the native Webshipper API, this operation is `POST /reports` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-report.md) for the provider-specific parameters and requirements.

