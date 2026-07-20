# Get file for view with Appwrite

Views a file from Appwrite storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/buckets/{bucketId}/files/{fileId}/view`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get file for view](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | path | `string` | yes | File ID. |
| `token` | query | `string` | no | File token for accessing this file. |
