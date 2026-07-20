# Update Custom Field with SendX

## Endpoint

- **Method:** `PUT`
- **Path:** `/customfield/:identifier`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [Update Custom Field](https://docs.sendx.io/api-reference/custom-field/update-custom-field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | path | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `number` | yes |
| `description` | body | `string` | yes |
