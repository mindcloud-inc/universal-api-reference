# Appwrite: Get bucket

Retrieves bucket details from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-bucket?connectionId=$CONNECTION_ID&bucketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-get-bucket?${params}`, {
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
| `bucketId` | string | yes | Bucket unique ID. |

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
      "allowedFileExtensions": [
        "string"
      ],
      "antivirus": true,
      "compression": "string",
      "enabled": true,
      "encryption": true,
      "fileSecurity": true,
      "maximumFileSize": 1,
      "name": "Ava Chen",
      "transformations": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Bucket creation time in ISO 8601 format. |
| `$id` | string | Bucket ID. |
| `$permissions` | array<string> | Bucket permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `$updatedAt` | string | Bucket update date in ISO 8601 format. |
| `allowedFileExtensions` | array<string> | Allowed file extensions. |
| `antivirus` | boolean | Virus scanning is enabled. |
| `compression` | string | Compression algorithm choosen for compression. Will be one of none, [gzip](https://en.wikipedia.org/wiki/Gzip), or [zstd](https://en.wikipedia.org/wiki/Zstd). |
| `enabled` | boolean | Bucket enabled. |
| `encryption` | boolean | Bucket is encrypted. |
| `fileSecurity` | boolean | Whether file-level security is enabled. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `maximumFileSize` | number | Maximum file size supported. |
| `name` | string | Bucket name. |
| `transformations` | boolean | Image transformations are enabled. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /storage/buckets/{bucketId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-get-bucket.md) for the provider-specific parameters and requirements.

