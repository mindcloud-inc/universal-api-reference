# Create file token with Appwrite

Creates a new file token in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens/buckets/{bucketId}/files/{fileId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create file token](https://appwrite.io/docs/references/cloud/server-rest/tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `fileId` | path | `string` | yes | File unique ID. |
| `expire` | body | `string` | no | Token expiry date |
