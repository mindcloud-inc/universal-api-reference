# Add File To Group with Pinata

Updates a Pinata group by adding a file.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/groups/:network/:id/ids/:fileId`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Add File To Group](https://docs.pinata.cloud/api-reference/endpoint/add-file-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | ID of the file to add to the group. |
| `id` | path | `string` | yes | ID of the target group. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
