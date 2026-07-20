# Microsoft 365 Excel: Replace Workbook Contents

Replaces workbook file contents in Microsoft 365 Excel.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/replace-workbook-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/replace-workbook-contents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "string",
  "driveItemId": "string",
  "workbookFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/replace-workbook-contents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "string",
    "driveItemId": "string",
    "workbookFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveId` | string | yes | Drive ID containing the workbook item. From Graph file output, use `parentReference.driveId`. |
| `driveItemId` | string | yes | Drive item ID of the workbook file to replace. From the output shown, this is the top-level `id`. |
| `workbookFile` | string | yes | Base64-encoded contents of a valid .xlsx workbook file. The action decodes this value and sends the raw workbook bytes to Microsoft Graph. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": {
        "mimeType": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "parentReference": {
        "driveId": "string",
        "id": "string"
      },
      "size": 1,
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file.mimeType` | string | Uploaded file MIME type. |
| `id` | string | Drive item ID of the uploaded workbook. |
| `name` | string | Workbook filename. |
| `parentReference.driveId` | string | Drive ID containing the workbook. |
| `parentReference.id` | string | Parent folder drive item ID. |
| `size` | number | Uploaded file size in bytes. |
| `webUrl` | string | URL to open the workbook. |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `PUT /v1.0/drives/:driveId/items/:driveItemId/content` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-workbook-contents.md) for the provider-specific parameters and requirements.

