# NocoDB: Upload Attachment to Cell

Uploads an attachment to a NocoDB cell.

```
POST https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/upload-attachment-to-cell
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/upload-attachment-to-cell" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "modelId": "string",
  "recordId": "string",
  "fieldId": "string",
  "contentType": "string",
  "file": "string",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/upload-attachment-to-cell', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "modelId": "string",
    "recordId": "string",
    "fieldId": "string",
    "contentType": "string",
    "file": "string",
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes | Base identifier. |
| `modelId` | string | yes | Model identifier. |
| `recordId` | string | yes | Record identifier. |
| `fieldId` | string | yes | Field identifier. |
| `contentType` | string | yes | Attachment content type. |
| `file` | string | yes | Base64-encoded file content. |
| `filename` | string | yes | Original filename. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedAt": "string",
      "fields": {},
      "id": 1,
      "UpdatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedAt` | string |  |
| `fields` | object |  |
| `id` | number |  |
| `UpdatedAt` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `POST /api/v3/data/:baseId/:modelId/records/:recordId/fields/:fieldId/upload` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment-to-cell.md) for the provider-specific parameters and requirements.

