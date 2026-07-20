# Openlayer: Create Storage Upload URL

Creates a storage upload URL in Openlayer.

```
POST https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-storage-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-storage-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectName": "mindcloud-upload-runtime.bin"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-storage-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectName": "mindcloud-upload-runtime.bin"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectName` | string | yes | Object name to upload. Default: `mindcloud-upload-runtime.bin`. |
| `workspaceId` | string | no | Workspace scope for the upload URL. Default: `b9ef2789-e1dd-4946-9ab0-189dcee20750`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {
        "key": "string",
        "policy": "string"
      },
      "storageUri": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields.key` | string |  |
| `fields.policy` | string |  |
| `storageUri` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `POST /storage/presigned-url` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-storage-upload-url.md) for the provider-specific parameters and requirements.

