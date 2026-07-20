# AlgoDocs: Upload Document From URL

Creates a document in AlgoDocs from a public URL.

```
POST https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AlgoDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": "string",
  "folderId": "string",
  "url": "https://api.algodocs.com/content/SampleInvoice.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/upload-document-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": "string",
    "folderId": "string",
    "url": "https://api.algodocs.com/content/SampleInvoice.pdf"
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
| `url` | string | yes | A publicly available URL for the file to upload. Example: `https://api.algodocs.com/content/SampleInvoice.pdf`. |

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

Through the native AlgoDocs API, this operation is `POST /document/upload_url/:extractorId/:folderId` (base URL `https://api.algodocs.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-from-url.md) for the provider-specific parameters and requirements.

