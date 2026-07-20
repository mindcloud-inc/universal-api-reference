# Typless: Extract Data Async



```
POST https://connect.mindcloud.co/v1/universal/typless/latest/actions/extract-data-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typless/latest/actions/extract-data-async" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/typless/latest/actions/extract-data-async', {
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
| `file_name` | string | yes | Original filename of the document being extracted asynchronously. |
| `file` | string | yes | Base64-encoded file content to extract asynchronously. |
| `document_type_name` | string | yes | Typless document type name to use for asynchronous extraction. |
| `parse_text_blocks` | boolean | no | Whether Typless should parse text blocks during async extraction. |
| `customer` | string | no | Optional customer identifier for the async extraction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extraction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extraction_id` | string | Typless extraction job identifier returned by async extraction. |

## Native endpoint

Through the native Typless API, this operation is `POST /api/v1/extract-data-async` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-async.md) for the provider-specific parameters and requirements.

