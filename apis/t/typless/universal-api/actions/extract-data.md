# Typless: Extract Data



```
POST https://connect.mindcloud.co/v1/universal/typless/latest/actions/extract-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typless/latest/actions/extract-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "Ava Chen",
  "file": "string",
  "document_type_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typless/latest/actions/extract-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "Ava Chen",
    "file": "string",
    "document_type_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | Original filename of the document being extracted. |
| `file` | string | yes | Base64-encoded file content to extract. |
| `document_type_name` | string | yes | Typless document type name to use for extraction. |
| `customer` | string | no | Optional customer identifier for the extraction. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "object_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | string | Customer associated with the extraction, when provided. |
| `extracted_fields` | array<object> | Extracted metadata fields returned by Typless. |
| `file_name` | string | Original file name of the extracted document. |
| `line_items` | array<array> | Extracted line item groups returned by Typless. |
| `object_id` | string | Typless extracted document object identifier. |

## Native endpoint

Through the native Typless API, this operation is `POST /api/v1/extract-data` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data.md) for the provider-specific parameters and requirements.

