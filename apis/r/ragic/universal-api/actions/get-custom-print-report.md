# Ragic: Get Custom Print Report

Retrieves a custom print report from Ragic.

```
GET https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-custom-print-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-custom-print-report?connectionId=$CONNECTION_ID&tabFolderPath=ragic-setup&sheetIndex=8&recordId=0&fileFormat=pdf&ragicCustomPrintTemplateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8",
  "recordId": "0",
  "fileFormat": "pdf",
  "ragicCustomPrintTemplateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-custom-print-report?${params}`, {
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
| `tabFolderPath` | string | yes | The folder path from the Ragic URL, for example `ragic-setup`. Default: `ragic-setup`. |
| `sheetIndex` | number | yes | The sheet number from the Ragic URL. Default: `8`. |
| `recordId` | number | yes | The record ID from the Ragic record URL. Default: `0`. |
| `fileFormat` | string | yes | The export file format. Supported values are `pdf`, `png`, and `docx`. Default: `pdf`. |
| `ragicCustomPrintTemplateId` | number | yes | The Custom Print Report template ID copied from a Ragic download URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileNameRefDomainId` | number | no | Optional field ID whose value will be used as the downloaded file name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `type` | string |  |

## Native endpoint

Through the native Ragic API, this operation is `GET /:tabFolderPath/:sheetIndex/:recordId.carbone` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-print-report.md) for the provider-specific parameters and requirements.

