# Delete File by ID with Pinata

Deletes an existing file from Pinata by ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/files/:network/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Delete File by ID](https://docs.pinata.cloud/api-reference/endpoint/delete-file-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the target file. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
