# Update Brand Color Tags with Orshot

## Endpoint

- **Method:** `PATCH`
- **Path:** `/brand-assets/colors/update/:id`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Update Brand Color Tags](https://orshot.com/docs/api-reference/brand-colors-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The saved brand color ID. |
| `tags[]` | body | `array<string>` | yes | The tags to set on the color, replacing existing tags. |
