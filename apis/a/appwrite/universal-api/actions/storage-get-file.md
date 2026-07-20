# Appwrite: Get file

Retrieves file details from Appwrite storage.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-file?connectionId=$CONNECTION_ID&bucketId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-file?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | string | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | string | yes | File ID. |

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

Through the native Appwrite API, this operation is `GET /storage/buckets/{bucketId}/files/{fileId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-get-file.md) for the provider-specific parameters and requirements.

