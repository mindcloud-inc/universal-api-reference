# PdfFiller: Create Template Constructor Link

Creates a constructor link for a PdfFiller template.

```
POST https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-template-constructor-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-template-constructor-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-template-constructor-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The document template identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_logo_id": 1,
      "document_id": 1,
      "hash": "string",
      "redirect_url": "https://example.com",
      "short_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_logo_id` | number |  |
| `document_id` | number |  |
| `hash` | string |  |
| `redirect_url` | string |  |
| `short_url` | string |  |
| `url` | string |  |

## Native endpoint

Through the native PdfFiller API, this operation is `POST /v2/templates/:templateId/constructor` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-constructor-link.md) for the provider-specific parameters and requirements.

