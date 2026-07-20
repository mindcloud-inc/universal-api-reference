# List files with Appwrite

Retrieves a list of files from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/buckets/{bucketId}/files`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List files](https://appwrite.io/docs/references/cloud/server-rest/storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Storage bucket unique ID. You can create a new storage bucket using the Storage service [server integration](https://appwrite.io/docs/server/storage#createBucket). |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: name, signature, mimeType, sizeOriginal, chunksTotal, chunksUploaded Send multiple values as a array. |
| `search` | query | `string` | no | Search term to filter your list results. Max length: 256 chars. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
