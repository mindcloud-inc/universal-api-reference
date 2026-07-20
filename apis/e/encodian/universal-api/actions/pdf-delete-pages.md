# Encodian: PDF Delete Pages

Deletes PDF pages in Encodian.

```
DELETE https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-delete-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-delete-pages?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-delete-pages?${params}`, {
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
| `fileContent` | string | yes | The file content of the source PDF file. |
| `startPage` | string | no | Set the page number to begin deleting pages from. |
| `endPage` | string | no | Set the page number to stop deleting pages on. |
| `pageNumbers` | string | no | A comma separated list of page numbers to delete, for example 1,3,4. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Any error messages returned by the operation. |
| `FileContent` | string | The processed PDF content in Base64. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Indicates whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/DeletePdfPages` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-delete-pages.md) for the provider-specific parameters and requirements.

