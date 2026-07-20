# Xodo Sign: Validate Bulk Sending CSV

Validates a bulk sending CSV for a template in Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/validate-bulk-sending-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/validate-bulk-sending-csv?connectionId=$CONNECTION_ID&business_id=string&templateHash=string&csv_with_bulk_data=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_id": "string",
  "templateHash": "string",
  "csv_with_bulk_data": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/validate-bulk-sending-csv?${params}`, {
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
| `business_id` | string | yes | The Xodo Sign business ID that owns the template. |
| `templateHash` | string | yes | The template hash to validate the CSV against. |
| `csv_with_bulk_data` | file | yes | The CSV file to validate as multipart form-data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "validated_rows": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `validated_rows` | array<array> | Validated bulk-send rows prepared in the JSON structure expected by Create Bulk Job. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /template/:templateHash/bulk/csv/validate` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-bulk-sending-csv.md) for the provider-specific parameters and requirements.

