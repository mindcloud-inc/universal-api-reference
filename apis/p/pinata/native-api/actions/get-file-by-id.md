# Get File by ID with Pinata

Retrieves a file from Pinata by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/files/:network/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Get File by ID](https://docs.pinata.cloud/api-reference/endpoint/get-file-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the target file. |
| `network` | path | `string` | yes | Target network (`public` or `private`). |
