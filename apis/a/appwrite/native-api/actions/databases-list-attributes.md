# List attributes with Appwrite

Retrieves a list of attributes from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List attributes](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: key, type, size, required, array, status, error Send multiple values as a array. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
