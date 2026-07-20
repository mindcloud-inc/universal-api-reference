# PDFMonkey: Get Template

Retrieves a template from PDFMonkey.

```
GET https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-template?connectionId=$CONNECTION_ID&id=BD22B61C-FDF2-42F1-B56A-1FE18C3C2E40" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "BD22B61C-FDF2-42F1-B56A-1FE18C3C2E40"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-template?${params}`, {
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
| `id` | string | yes | ID of the template to fetch. Example: `BD22B61C-FDF2-42F1-B56A-1FE18C3C2E40`. |

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

Through the native PDFMonkey API, this operation is `GET /document_templates/:id` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

