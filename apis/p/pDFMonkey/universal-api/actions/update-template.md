# PDFMonkey: Update Template

Updates an existing template in PDFMonkey.

```
PUT https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "3e642963-37eb-43ec-a6f5-71be4514b26b",
  "pdfEngineDraftId": "c1931951-3a89-4066-9eb7-0adce6c9dcc8"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "3e642963-37eb-43ec-a6f5-71be4514b26b",
    "pdfEngineDraftId": "c1931951-3a89-4066-9eb7-0adce6c9dcc8"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the template to update. Example: `3e642963-37eb-43ec-a6f5-71be4514b26b`. |
| `identifier` | string | no | Human name of the document template. Example: `Stage 3 Template`. |
| `editionMode` | string | no | Template editing mode. Default: `code`. Example: `code`. |
| `bodyDraft` | string | no | Draft HTML + Liquid content. Example: `<p>Hello {{name}}</p>`. |
| `scssStyleDraft` | string | no | Draft CSS or SCSS style. Example: `body { font-family: sans-serif; }`. |
| `sampleDataDraft` | string | no | Draft sample data as a JSON string. Example: `[object Object]`. |
| `settingsDraft` | object | no | Draft template settings object. Example: `[object Object]`. |
| `pdfEngineDraftId` | string | yes | PDF engine used to preview draft changes. Example: `c1931951-3a89-4066-9eb7-0adce6c9dcc8`. |
| `ttl` | number | no | Document expiration delay in seconds. Default: `86400`. Example: `86400`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentTemplate": {
        "appId": "string",
        "body": "string",
        "bodyDraft": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deletedAt": "2026-05-07T12:00:00.000Z",
        "editionMode": "string",
        "id": "string",
        "identifier": "string",
        "outputType": "string",
        "pdfEngineDraftId": "string",
        "pdfEngineId": "string",
        "previewUrl": "https://example.com",
        "sampleData": "string",
        "sampleDataDraft": "string",
        "scssStyle": "string",
        "scssStyleDraft": "string",
        "settings": {},
        "settingsDraft": {},
        "templateFolderId": "string",
        "ttl": 1,
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
| `documentTemplate.appId` | string | Owning workspace ID. |
| `documentTemplate.body` | string | Published template body. |
| `documentTemplate.bodyDraft` | string | Draft template body. |
| `documentTemplate.createdAt` | date | Creation timestamp. |
| `documentTemplate.deletedAt` | date | Deletion timestamp when present. |
| `documentTemplate.editionMode` | string | Template editing mode. |
| `documentTemplate.id` | string | Template ID. |
| `documentTemplate.identifier` | string | Template name. |
| `documentTemplate.outputType` | string | Generated file output type. |
| `documentTemplate.pdfEngineDraftId` | string | Draft PDF engine ID. |
| `documentTemplate.pdfEngineId` | string | Published PDF engine ID. |
| `documentTemplate.previewUrl` | string | Template preview URL. |
| `documentTemplate.sampleData` | string | Published sample data. |
| `documentTemplate.sampleDataDraft` | string | Draft sample data. |
| `documentTemplate.scssStyle` | string | Published template style. |
| `documentTemplate.scssStyleDraft` | string | Draft template style. |
| `documentTemplate.settings` | object | Published template settings. |
| `documentTemplate.settingsDraft` | object | Draft template settings. |
| `documentTemplate.templateFolderId` | string | Template folder ID when present. |
| `documentTemplate.ttl` | number | Document expiration delay. |
| `documentTemplate.updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native PDFMonkey API, this operation is `PUT /document_templates/:id` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

