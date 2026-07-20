# Remove File From Group with Pinata

Deletes a file from a Pinata group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/groups/:network/:id/ids/:fileId`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Remove File From Group](https://docs.pinata.cloud/api-reference/endpoint/remove-file-from-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | ID of the file to remove from the group. |
| `id` | path | `string` | yes | ID of the target group. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
