# Typless: Get Extraction Data



```
GET https://connect.mindcloud.co/v1/universal/typless/latest/actions/get-extraction-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typless/latest/actions/get-extraction-data?connectionId=$CONNECTION_ID&extraction_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extraction_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typless/latest/actions/get-extraction-data?${params}`, {
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
| `extraction_id` | string | yes | Typless extraction job identifier. |
| `text_blocks` | boolean | no | Whether to include text block details in the extraction response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "result": {
        "customer": "string",
        "extracted_fields": [
          {}
        ],
        "file_name": "Ava Chen",
        "line_items": [
          [
            "string"
          ]
        ],
        "object_id": "string",
        "vat_rates": [
          {}
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object | Error information when extraction fails. |
| `result.customer` | string | Customer associated with the extraction, when provided. |
| `result.extracted_fields` | array<object> | Extracted metadata fields returned by Typless. |
| `result.file_name` | string | Original file name of the extracted document. |
| `result.line_items` | array<array> | Extracted line item groups. |
| `result.object_id` | string | Typless extracted document object identifier. |
| `result.vat_rates` | array<object> | Extracted VAT rate groups. |
| `status` | string | Extraction job status. |

## Native endpoint

Through the native Typless API, this operation is `GET /api/v1/get-extraction-data` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extraction-data.md) for the provider-specific parameters and requirements.

