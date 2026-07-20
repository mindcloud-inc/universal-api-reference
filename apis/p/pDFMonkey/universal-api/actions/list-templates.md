# PDFMonkey: List Templates

Retrieves templates from PDFMonkey.

```
GET https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/list-templates?connectionId=$CONNECTION_ID&workspaceId=99fcc9d4-ae24-459c-b8d2-2cd696519a7d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "99fcc9d4-ae24-459c-b8d2-2cd696519a7d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/list-templates?${params}`, {
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
| `workspaceId` | string | yes | Workspace to search within. Example: `99fcc9d4-ae24-459c-b8d2-2cd696519a7d`. |
| `folders` | string | no | Comma-separated folder IDs to search within, or none for the root folder. Example: `none`. |
| `page` | number | no | Page number to return. Example: `1`. |
| `sort` | string | no | Attribute to sort by: identifier, created_at, or updated_at. Example: `identifier`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentTemplateCard": {
        "appId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "editionMode": "string",
        "id": "string",
        "identifier": "string",
        "isDraft": true,
        "outputType": "string",
        "pdfEngineDeprecatedOn": "2026-05-07T12:00:00.000Z",
        "pdfEngineName": "Ava Chen",
        "templateFolderId": "string",
        "templateFolderIdentifier": "string",
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
| `documentTemplateCard.appId` | string | Owning workspace ID. |
| `documentTemplateCard.createdAt` | date | Creation timestamp. |
| `documentTemplateCard.editionMode` | string | Template editing mode. |
| `documentTemplateCard.id` | string | Document template ID. |
| `documentTemplateCard.identifier` | string | Template name. |
| `documentTemplateCard.isDraft` | boolean | Whether the template has unpublished changes. |
| `documentTemplateCard.outputType` | string | Generated file output type. |
| `documentTemplateCard.pdfEngineDeprecatedOn` | date | PDF engine deprecation date when present. |
| `documentTemplateCard.pdfEngineName` | string | PDF engine name. |
| `documentTemplateCard.templateFolderId` | string | Folder ID when present. |
| `documentTemplateCard.templateFolderIdentifier` | string | Folder name when present. |
| `documentTemplateCard.updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native PDFMonkey API, this operation is `GET /document_template_cards` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

