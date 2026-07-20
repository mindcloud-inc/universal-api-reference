# Veryfi: Process a Contract

Creates a new contract in Veryfi.

```
POST https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-contracts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-contracts', {
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
| `maxPagesToProcess` | number | no | Possible values: >= 1 and <= 50 Default value: 50 Limit processing to number of pages. A page is a pdf page or an image |
| `autoDelete` | boolean | no | Default value: false Delete this contract from Veryfi after data has been extracted |
| `fileData` | string | no | Possible values: non-empty The least effective way to submit files. Base64 encoded string, could be raw or datauri https://en.wikipedia.org/wiki/Data_URI_scheme E.g. 'data:application/zip;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVQYV2NgYAAAAAMAAWgmWQ0AAAAASUVORK5CYII=' |
| `fileUrl` | string | no | Possible values: non-empty |
| `packagePath` | string | no | Possible values: non-empty A path to file in S3 bucket, e.g. 'some/contract.pdf |
| `bucket` | string | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'contracts' |
| `fileName` | string | no | Possible values: non-empty Optional filename, helps to determine file type |
| `metaExternalId` | string | no | Possible values: non-empty External ID you want to associate with the document. |
| `metaTags[]` | array<string> | no | Possible values: non-empty Default value: `` Tags you want to associate with the document. |
| `externalId` | string | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `fileUrls[]` | array<string> | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file` | string | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        {}
      ],
      "error": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | array<object> |  |
| `error` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `POST /api/v8/partner/contracts` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-v8-partner-contracts.md) for the provider-specific parameters and requirements.

