# Appwrite: Update file

Updates the file in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": "string",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-update-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": "string",
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | string | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `permissions` | string | no | An array of permission string. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `fileId` | string | yes | File unique ID. |
| `name` | string | no | Name of the file |
| `permissions[]` | array<string> | no | An array of permission string. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |

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
| `$createdAt` | string | File creation date in ISO 8601 format. |
| `$id` | string | File ID. |
| `$permissions` | array<string> | File permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `$updatedAt` | string | File update date in ISO 8601 format. |
| `bucketId` | string | Bucket ID. |
| `chunksTotal` | number | Total number of chunks available |
| `chunksUploaded` | number | Total number of chunks uploaded |
| `mimeType` | string | File mime type. |
| `name` | string | File name. |
| `signature` | string | File MD5 signature. |
| `sizeOriginal` | number | File original size in bytes. |

## Native endpoint

Through the native Appwrite API, this operation is `PUT /storage/buckets/{bucketId}/files/{fileId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-update-file.md) for the provider-specific parameters and requirements.

