# Update Plugin Metadata with Port API AI

Updates plugin metadata in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/plugins/:identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Plugin Metadata](https://docs.port.io/api-reference/update-metadata-of-a-plugin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The Port plugin identifier. |
| `title` | body | `string` | yes | Plugin title. |
