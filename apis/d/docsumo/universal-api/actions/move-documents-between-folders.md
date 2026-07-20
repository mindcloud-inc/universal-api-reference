# Docsumo: Move Documents Between Folders

Moves documents between folders in Docsumo.

```
PUT https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/move-documents-between-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docsumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/move-documents-between-folders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dest_folder_id": "string",
  "doc_ids[]": [
    "string"
  ],
  "source_folder_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/move-documents-between-folders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dest_folder_id": "string",
    "doc_ids[]": ["string"],
    "source_folder_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dest_folder_id` | string | yes | Folder ID to move documents to. Use an empty string for My Documents. |
| `doc_ids[]` | array<string> | yes | One or more document IDs to move. |
| `source_folder_id` | string | yes | Folder ID to move documents from. Use an empty string for My Documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "error_code": "string",
      "message": "string",
      "source": "string",
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | string |  |
| `error_code` | string |  |
| `message` | string |  |
| `source` | string |  |
| `status` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native Docsumo API, this operation is `POST /api/v2/eevee/apikey/move/` (base URL `https://app.docsumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-documents-between-folders.md) for the provider-specific parameters and requirements.

