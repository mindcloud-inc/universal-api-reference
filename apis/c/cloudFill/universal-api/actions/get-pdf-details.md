# CloudFill: Get PDF Details

Retrieves PDF metadata and field details from CloudFill.

```
GET https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/get-pdf-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudFill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/get-pdf-details?connectionId=$CONNECTION_ID&pdfKey=pdf_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfKey": "pdf_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/get-pdf-details?${params}`, {
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
| `pdfKey` | string | yes | CloudFill PDF template key. Example: `pdf_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ],
      "variables": [
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
| `fields` | array<object> | Fields available in the PDF, including image fields. |
| `variables` | array<object> | Text variables that can be replaced during PDF generation. |

## Native endpoint

Through the native CloudFill API, this operation is `GET /api/meta/pdf/{pdfKey}` (base URL `https://api.cloudfill.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-details.md) for the provider-specific parameters and requirements.

