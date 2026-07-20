# Update bucket with Appwrite

Updates the bucket in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/storage/buckets/{bucketId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update bucket](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowedFileExtensions` | body | `string` | no | Allowed file extensions. Maximum of 100 extensions are allowed, each 64 characters long. |
| `bucketId` | path | `string` | yes | Bucket unique ID. |
| `permissions` | body | `string` | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `name` | body | `string` | yes | Bucket name |
| `permissions[]` | body | `array<string>` | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `fileSecurity` | body | `boolean` | no | Enables configuring permissions for individual file. A user needs one of file or bucket level permissions to access a file. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | body | `boolean` | no | Is bucket enabled? When set to 'disabled', users cannot access the files in this bucket but Server SDKs with and API key can still access the bucket. No files are lost when this is toggled. |
| `maximumFileSize` | body | `number` | no | Maximum file size allowed in bytes. Maximum allowed value is 30MB. |
| `allowedFileExtensions[]` | body | `array<string>` | no | Allowed file extensions. Maximum of 100 extensions are allowed, each 64 characters long. |
| `compression` | body | `string` | no | Compression algorithm choosen for compression. Can be one of none, [gzip](https://en.wikipedia.org/wiki/Gzip), or [zstd](https://en.wikipedia.org/wiki/Zstd), For file size above 20MB compression is skipped even if it's enabled |
| `encryption` | body | `boolean` | no | Is encryption enabled? For file size above 20MB encryption is skipped even if it's enabled |
| `antivirus` | body | `boolean` | no | Is virus scanning enabled? For file size above 20MB AntiVirus scanning is skipped even if it's enabled |
| `transformations` | body | `boolean` | no | Are image transformations enabled? |
