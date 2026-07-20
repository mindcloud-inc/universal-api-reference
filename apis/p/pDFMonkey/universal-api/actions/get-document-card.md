# PDFMonkey: Get Document Card

Retrieves a document card from PDFMonkey.

```
GET https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-document-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-document-card?connectionId=$CONNECTION_ID&id=0262787a-7c7d-43f6-a2f6-311f4695c9b3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0262787a-7c7d-43f6-a2f6-311f4695c9b3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-document-card?${params}`, {
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
| `id` | string | yes | ID of the Document to fetch. Example: `0262787a-7c7d-43f6-a2f6-311f4695c9b3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentCard": {
        "appId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "documentTemplateId": "string",
        "documentTemplateIdentifier": "string",
        "downloadUrl": "https://example.com",
        "failureCause": "string",
        "filename": "Ava Chen",
        "id": "string",
        "meta": "string",
        "outputType": "string",
        "previewUrl": "https://example.com",
        "publicShareLink": "https://example.com",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentCard.appId` | string | Owning PDFMonkey app ID. |
| `documentCard.createdAt` | date | Creation timestamp. |
| `documentCard.documentTemplateId` | string | Source template ID. |
| `documentCard.documentTemplateIdentifier` | string | Source template identifier. |
| `documentCard.downloadUrl` | string | Download URL. |
| `documentCard.failureCause` | string | Failure cause when generation does not succeed. |
| `documentCard.filename` | string | Generated file name. |
| `documentCard.id` | string | Document card ID. |
| `documentCard.meta` | string | Serialized document metadata. |
| `documentCard.outputType` | string | Generated file output type. |
| `documentCard.previewUrl` | string | Preview URL. |
| `documentCard.publicShareLink` | string | Public share URL. |
| `documentCard.status` | string | Generation status. |
| `documentCard.updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native PDFMonkey API, this operation is `GET /document_cards/:id` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-card.md) for the provider-specific parameters and requirements.

