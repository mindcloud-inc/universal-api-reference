# Lumin: Create Document



```
POST https://connect.mindcloud.co/v1/universal/lumin/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentName": "Ava Chen",
  "fileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lumin/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentName": "Ava Chen",
    "fileUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentName` | string | yes | Human-friendly title of the document. |
| `fileUrl` | string | yes | HTTPS URL for the source file to import into Lumin. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": {
        "createdAt": 1,
        "id": "string",
        "location": {
          "folderId": "string",
          "spaceId": "string",
          "type": "string",
          "workspaceId": "string"
        },
        "mimeType": "string",
        "name": "Ava Chen",
        "previewUrl": "https://example.com",
        "size": 1,
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document.createdAt` | number |  |
| `document.id` | string |  |
| `document.location.folderId` | string |  |
| `document.location.spaceId` | string |  |
| `document.location.type` | string |  |
| `document.location.workspaceId` | string |  |
| `document.mimeType` | string |  |
| `document.name` | string |  |
| `document.previewUrl` | string |  |
| `document.size` | number |  |
| `document.updatedAt` | number |  |

## Native endpoint

Through the native Lumin API, this operation is `POST /documents` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

