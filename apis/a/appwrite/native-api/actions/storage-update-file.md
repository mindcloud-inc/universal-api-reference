# Update file with Appwrite

Updates the file in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/storage/buckets/{bucketId}/files/{fileId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update file](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `permissions` | body | `string` | no | An array of permission string. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `fileId` | path | `string` | yes | File unique ID. |
| `name` | body | `string` | no | Name of the file |
| `permissions[]` | body | `array<string>` | no | An array of permission string. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
