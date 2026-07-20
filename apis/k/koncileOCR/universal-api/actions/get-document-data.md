# Koncile OCR: Get Document Data



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-document-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-document-data?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-document-data?${params}`, {
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
| `document_id` | string | yes | The document identifier to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": 1,
      "document_name": "Ava Chen",
      "General_fields": {},
      "General_fields_list": [
        {}
      ],
      "Line_fields": {},
      "task_id": "string",
      "template_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | number | The document identifier. |
| `document_name` | string | The original file name. |
| `General_fields` | object | General extracted fields keyed by field name. |
| `General_fields_list` | array<object> | General extracted fields as a list. |
| `Line_fields` | object | Line field extraction output. |
| `task_id` | string | The associated task identifier. |
| `template_id` | number | The template used for extraction. |

## Native endpoint

Through the native Koncile OCR API, this operation is `GET /fetch_document_data` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-data.md) for the provider-specific parameters and requirements.

