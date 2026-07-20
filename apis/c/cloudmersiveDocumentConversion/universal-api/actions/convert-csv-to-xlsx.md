# Cloudmersive Document Conversion: Convert CSV to XLSX

Converts a CSV file to XLSX.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-csv-to-xlsx
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Document Conversion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-csv-to-xlsx?connectionId=$CONNECTION_ID&inputFile=bmFtZSx2YWx1ZQpFeGFtcGxlLDEK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputFile": "bmFtZSx2YWx1ZQpFeGFtcGxlLDEK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-csv-to-xlsx?${params}`, {
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
| `inputFile` | file | yes | Input CSV file to convert to XLSX. Default: `bmFtZSx2YWx1ZQpFeGFtcGxlLDEK`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputFile` | string | Converted XLSX file content returned by Cloudmersive. |

## Native endpoint

Through the native Cloudmersive Document Conversion API, this operation is `POST /convert/csv/to/xlsx` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-csv-to-xlsx.md) for the provider-specific parameters and requirements.

