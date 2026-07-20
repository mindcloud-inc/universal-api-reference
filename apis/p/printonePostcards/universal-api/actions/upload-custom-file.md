# Print.one Postcards: Upload Custom File

Uploads a custom file to Print.one Postcards.

```
POST https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/upload-custom-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/upload-custom-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/upload-custom-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "id": "string",
      "metadata": {
        "height": "string",
        "type": "string",
        "width": "string"
      },
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `metadata.height` | string |  |
| `metadata.type` | string |  |
| `metadata.width` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `POST /v2/customfiles` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-custom-file.md) for the provider-specific parameters and requirements.

