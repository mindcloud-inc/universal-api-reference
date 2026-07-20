# List Form Comments with Wufoo

Retrieves comments from a specific Wufoo form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:identifier/comments.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [List Form Comments](https://wufoo.github.io/docs/#forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The form hash or identifier whose comments to list. |
