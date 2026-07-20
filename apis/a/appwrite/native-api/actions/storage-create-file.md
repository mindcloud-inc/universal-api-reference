# Create file with Appwrite

Creates a new file in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/buckets/{bucketId}/files`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create file](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | body | `string` | yes | File ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `file` | body | `file` | yes | Binary file. Appwrite SDKs provide helpers to handle file input. [Learn about file input](https://appwrite.io/docs/products/storage/upload-download#input-file). |
| `permissions[]` | body | `array<string>` | no | An array of permission strings. By default, only the current user is granted all permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
