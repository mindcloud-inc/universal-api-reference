# Get Group with Google Groups

Retrieves a Google Group by key.

## Endpoint

- **Method:** `GET`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Get Group](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
