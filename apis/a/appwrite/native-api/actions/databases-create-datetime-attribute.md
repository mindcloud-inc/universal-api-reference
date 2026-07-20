# Create datetime attribute with Appwrite

Creates a new datetime attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/datetime`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create datetime attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#createCollection). |
| `key` | body | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | no | Default value for the attribute in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. Cannot be set when attribute is required. |
| `array` | body | `boolean` | no | Is attribute an array? |
