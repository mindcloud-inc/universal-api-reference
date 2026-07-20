# Appwrite: Create file

Creates a new file in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": "string",
  "fileId": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": "string",
    "fileId": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | string | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | string | yes | File ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `file` | file | yes | Binary file. Appwrite SDKs provide helpers to handle file input. [Learn about file input](https://appwrite.io/docs/products/storage/upload-download#input-file). |
| `permissions[]` | array<string> | no | An array of permission strings. By default, only the current user is granted all permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$permissions": [
        "string"
      ],
      "$updatedAt": "string",
      "bucketId": "string",
      "chunksTotal": 1,
      "chunksUploaded": 1,
      "mimeType": "string",
      "name": "Ava Chen",
      "signature": "string",
      "sizeOriginal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string |  |
| `$id` | string |  |
| `$permissions` | array<string> |  |
| `$updatedAt` | string |  |
| `bucketId` | string |  |
| `chunksTotal` | number |  |
| `chunksUploaded` | number |  |
| `mimeType` | string |  |
| `name` | string |  |
| `signature` | string |  |
| `sizeOriginal` | number |  |

## Native endpoint

Through the native Appwrite API, this operation is `POST /storage/buckets/{bucketId}/files` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-create-file.md) for the provider-specific parameters and requirements.

