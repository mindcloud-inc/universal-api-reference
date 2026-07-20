# Appwrite: Create bucket

Creates a new bucket in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-create-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-create-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/storage-create-bucket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedFileExtensions` | string | no | Allowed file extensions. Maximum of 100 extensions are allowed, each 64 characters long. |
| `bucketId` | string | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `permissions` | string | no | An array of permission strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `name` | string | yes | Bucket name |
| `permissions[]` | array<string> | no | An array of permission strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `fileSecurity` | boolean | no | Enables configuring permissions for individual file. A user needs one of file or bucket level permissions to access a file. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | boolean | no | Is bucket enabled? When set to 'disabled', users cannot access the files in this bucket but Server SDKs with and API key can still access the bucket. No files are lost when this is toggled. |
| `maximumFileSize` | number | no | Maximum file size allowed in bytes. Maximum allowed value is 30MB. |
| `allowedFileExtensions[]` | array<string> | no | Allowed file extensions. Maximum of 100 extensions are allowed, each 64 characters long. |
| `compression` | string | no | Compression algorithm choosen for compression. Can be one of none, [gzip](https://en.wikipedia.org/wiki/Gzip), or [zstd](https://en.wikipedia.org/wiki/Zstd), For file size above 20MB compression is skipped even if it's enabled |
| `encryption` | boolean | no | Is encryption enabled? For file size above 20MB encryption is skipped even if it's enabled |
| `antivirus` | boolean | no | Is virus scanning enabled? For file size above 20MB AntiVirus scanning is skipped even if it's enabled |
| `transformations` | boolean | no | Are image transformations enabled? |

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

Through the native Appwrite API, this operation is `POST /storage/buckets` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-create-bucket.md) for the provider-specific parameters and requirements.

