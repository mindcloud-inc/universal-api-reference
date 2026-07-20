# Stencil: Get PDF



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-pdf?connectionId=$CONNECTION_ID&pdfId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-pdf?${params}`, {
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
| `pdfId` | string | yes | PDF generation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "log": "string",
      "metadata": {},
      "modifications": [
        {}
      ],
      "pdfUrl": "https://example.com",
      "self": "string",
      "status": "string",
      "templateId": "string",
      "webhookResponseBody": "string",
      "webhookResponseCode": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `log` | string |  |
| `metadata` | object |  |
| `modifications` | array<object> |  |
| `pdfUrl` | string |  |
| `self` | string |  |
| `status` | string |  |
| `templateId` | string |  |
| `webhookResponseBody` | string |  |
| `webhookResponseCode` | number |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Stencil API, this operation is `GET /v1/pdfs/:pdf_id` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf.md) for the provider-specific parameters and requirements.

