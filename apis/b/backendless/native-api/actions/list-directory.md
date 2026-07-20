# List Directory with Backendless

Retrieves a directory listing from Backendless.

## Endpoint

- **Method:** `GET`
- **Path:** `/{applicationId}/{apiKey}/files/{path}/`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [List Directory](https://backendless.com/docs/rest/file_directory_listing.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Directory path to list. Leave blank to list the root files directory. |
