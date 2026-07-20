# Encodian: PDF Extract Text By Page

Extracts PDF text by page in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-text-by-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-text-by-page?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/p-df-extract-text-by-page?${params}`, {
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
| `fileContent` | string | yes | A Base64 encoded representation of the PDF file to be processed. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startPage` | number | no | Sets the page number to begin text extraction from. |
| `endPage` | number | no | Sets the page number to end text extraction from. |
| `pageNumbers` | string | no | A comma-separated list of page numbers to extract. Example: `1,3,4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "Pages": [
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
| `Errors` | array<string> | Errors returned by Encodian, if any. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |
| `Pages` | array<object> | The collection of text values extracted by page. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/PdfExtractTextByPage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/p-df-extract-text-by-page.md) for the provider-specific parameters and requirements.

