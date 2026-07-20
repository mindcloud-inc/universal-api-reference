# Get file with Appwrite

Retrieves file details from Appwrite storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/buckets/{bucketId}/files/{fileId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get file](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | path | `string` | yes | File ID. |
