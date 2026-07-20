# AlgoDocs: Upload Document With Base64

Creates a document in AlgoDocs from base64 content.

```
POST https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-with-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AlgoDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-with-base64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": "string",
  "folderId": "string",
  "fileBase64": "string",
  "filename": "SampleDocument.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-with-base64', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": "string",
    "folderId": "string",
    "fileBase64": "string",
    "filename": "SampleDocument.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractorId` | string | yes | The extractor ID from your AlgoDocs account. |
| `folderId` | string | yes | The folder ID where the uploaded document should be saved. |
| `fileBase64` | string | yes | The base64-encoded file contents. |
| `filename` | string | yes | The file name to associate with the uploaded base64 document. Example: `SampleDocument.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileMD5CheckSum": "string",
      "fileSize": 1,
      "id": 1,
      "uploadedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileMD5CheckSum` | string |  |
| `fileSize` | number |  |
| `id` | number |  |
| `uploadedAt` | date |  |

## Native endpoint

Through the native AlgoDocs API, this operation is `POST /document/upload_base64/:extractorId/:folderId` (base URL `https://api.algodocs.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-with-base64.md) for the provider-specific parameters and requirements.

