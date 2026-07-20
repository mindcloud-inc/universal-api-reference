# Update Brand Asset Image Tags with Orshot

## Endpoint

- **Method:** `PATCH`
- **Path:** `/brand-assets/images/update/:id`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Update Brand Asset Image Tags](https://orshot.com/docs/api-reference/brand-assets-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The brand asset image ID. |
| `tags[]` | body | `array<string>` | yes | The tags to set on the asset, replacing existing tags. |
