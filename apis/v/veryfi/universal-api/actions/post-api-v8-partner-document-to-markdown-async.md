# Veryfi: Process a Markdown Document asynchronously

Creates a new markdown document asynchronously in Veryfi.

```
POST https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-document-to-markdown-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-document-to-markdown-async" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-document-to-markdown-async', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoDelete` | boolean | no | Default value: false Whether to delete the document after processing. In async deletes the document after the first GET request. |
| `details` | boolean | no |  |
| `documentType` | string | no | Default value: document |
| `externalId` | string | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `tags[]` | array<string> | no |  |
| `maxPagesToProcess` | number | no | Possible values: >= 1 and <= 50 Default value: 50 |
| `metaTags[]` | array<string> | no | Possible values: non-empty Default value: `` Tags you want to associate with the document. |
| `packagePath` | string | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | string | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `fileData` | string | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `fileUrl` | string | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `fileUrls[]` | array<string> | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `fileName` | string | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `metaExternalId` | string | no | Possible values: non-empty External ID you want to associate with the document. |
| `file` | string | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Veryfi API, this operation is `POST /api/v8/partner/document-to-markdown/async` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-v8-partner-document-to-markdown-async.md) for the provider-specific parameters and requirements.

