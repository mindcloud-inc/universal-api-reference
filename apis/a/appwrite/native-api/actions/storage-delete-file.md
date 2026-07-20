# Delete file with Appwrite

Deletes the file from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/storage/buckets/{bucketId}/files/{fileId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete file](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | path | `string` | yes | File ID. |
