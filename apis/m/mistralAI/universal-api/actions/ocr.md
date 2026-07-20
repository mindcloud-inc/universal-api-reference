# Mistral AI: OCR

Creates OCR results for a document in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/ocr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/ocr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "document": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/ocr', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "document": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | OCR model ID. |
| `document` | object | yes | Document source object to run OCR on. |
| `id` | string | no | Optional client identifier for the OCR request. |
| `pages[]` | array<number> | no | Specific page numbers to process. |
| `includeImageBase64` | boolean | no | Include extracted image content in the response. |
| `imageLimit` | number | no | Maximum number of images to extract. |
| `imageMinSize` | number | no | Minimum image size threshold for extraction. |
| `bboxAnnotationFormat` | object | no | Structured output format for extracted bounding boxes or images. |
| `documentAnnotationFormat` | object | no | Structured output format for the full document. |
| `documentAnnotationPrompt` | string | no | Prompt that guides document-level structured extraction. |
| `tableFormat` | string | no | Table output format such as markdown or html. |
| `extractHeader` | boolean | no | Whether to extract document header regions. |
| `extractFooter` | boolean | no | Whether to extract document footer regions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_annotation": {},
      "model": "string",
      "pages": [
        {}
      ],
      "usage_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_annotation` | object |  |
| `model` | string |  |
| `pages` | array<object> |  |
| `usage_info` | object |  |

## Native endpoint

Through the native Mistral AI API, this operation is `POST /v1/ocr` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ocr.md) for the provider-specific parameters and requirements.

