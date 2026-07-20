# PDF-app: Extract Data From PDF

Retrieves extracted data from a PDF in PDF-app.

```
GET https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/extract-data-from-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/extract-data-from-pdf?connectionId=$CONNECTION_ID&fileUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/extract-data-from-pdf?${params}`, {
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
| `fileUrl` | string | yes | Public URL of the PDF file to extract data from. |
| `templateId` | string | no | Optional extraction template ID. |
| `async` | boolean | no | Run the extraction asynchronously and fetch the result later by job ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content[].name` | string | no | Label for one extraction region. |
| `content[].rectangle` | string | no | Rectangle coordinates for one extraction region, for example {65, 69, 196, 21}. |
| `content[].page` | number | no | Page number for one extraction region. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "extraction_results": [
        "string"
      ],
      "job_id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `creditsRemaining` | number |  |
| `extraction_results` | array |  |
| `job_id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PDF-app API, this operation is `POST /extract_pdf_to_data_py` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-pdf.md) for the provider-specific parameters and requirements.

