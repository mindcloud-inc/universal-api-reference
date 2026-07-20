# Natif.ai: Get OCR Results

Retrieves OCR results for a document from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-ocr-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-ocr-results?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-ocr-results?${params}`, {
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
| `documentId` | string | yes | UUID of the document. |
| `ocrFormat` | list | no | Format of the returned OCR results. One of: `HOCR`, `Natif`. Default: `natif`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFulltext` | boolean | no | Return page text content as a string for the natif OCR format. |
| `includeTransformations` | boolean | no | Return rotation and cropping transformations. Cannot be combined with Include Fulltext. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "pages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | hOCR HTML when OCR Format is hocr. |
| `pages` | array<object> | OCR page data for Natif-format responses. |

## Native endpoint

Through the native Natif.ai API, this operation is `GET /documents/[:documentId]/ocr` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ocr-results.md) for the provider-specific parameters and requirements.

