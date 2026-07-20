# Update File with Pinata

Updates an existing file in Pinata.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/files/:network/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Update File](https://docs.pinata.cloud/api-reference/endpoint/update-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the target file. |
| `name` | body | `string` | no | Updated name for the target file. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
