# PdfFiller: List Template Child Documents

Retrieves filled documents for a PdfFiller template.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-template-child-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-template-child-documents?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-template-child-documents?${params}`, {
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
| `templateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "next_page_url": "https://example.com",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `next_page_url` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/templates/:templateId/filled_documents` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-child-documents.md) for the provider-specific parameters and requirements.

