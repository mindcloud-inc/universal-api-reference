# PDF-app: Edit PDF

Updates a PDF with edits in PDF-app.

```
PUT https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/edit-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/edit-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/edit-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | PDF file URL to edit. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `async` | boolean | no | Whether to run PDF editing asynchronously. Default: `false`. |
| `annotations[]` | array<object> | no | Text annotations to add to the PDF. Example: `[object Object]`. |
| `images[]` | array<object> | no | Images to insert into the PDF. Example: `[object Object]`. |
| `remove_elements[]` | array<object> | no | Regions to clear from the PDF. Example: `[object Object]`. |
| `search_texts[]` | array<object> | no | Search-and-replace operations for text in the PDF. Example: `[object Object]`. |
| `fileName` | string | no | Desired file name for the edited PDF output. Example: `edited-dummy`. |
| `deletePages[]` | array<number> | no | Page numbers to delete from the PDF. Example: `2,4`. |
| `moveContent[]` | array<object> | no | Content transformations to apply to rectangular areas of the PDF. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "job_id": "string",
      "message": "string",
      "presignedUrls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number | Credits consumed by the PDF edit request. |
| `creditsRemaining` | number | Remaining provider credits after the edit request. |
| `job_id` | string | Provider job identifier for the edit request. |
| `message` | string | Summary of the PDF edit result. |
| `presignedUrls` | array<string> | Temporary download URLs for the edited PDF output. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /edit_pdf` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-pdf.md) for the provider-specific parameters and requirements.

