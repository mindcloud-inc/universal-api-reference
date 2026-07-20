# Stencil: Create PDF



```
POST https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modifications[]": [
    {}
  ],
  "template": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modifications[]": [{}],
    "template": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Extra metadata to include with the result. |
| `modifications[]` | array<object> | yes | Array of modification objects. |
| `template` | string | yes | Template ID to generate a PDF from. |
| `webhookUrl` | string | no | Webhook URL called when PDF generation completes. |

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

Through the native Stencil API, this operation is `POST /v1/pdfs` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf.md) for the provider-specific parameters and requirements.

