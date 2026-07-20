# Update Company with Nutshell

Updates an existing company in Nutshell.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:id`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Update Company](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Nutshell company ID to update. |
| `patches[].op` | body | `string` | no | JSON Patch operation to perform. |
| `patches[].path` | body | `string` | no | JSON Pointer path to update. |
| `patches[].value` | body | `string` | no | Value to apply for the patch operation. |
