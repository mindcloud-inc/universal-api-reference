# Add Brand Color with Orshot

## Endpoint

- **Method:** `POST`
- **Path:** `/brand-assets/colors/add`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Add Brand Color](https://orshot.com/docs/api-reference/brand-colors-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The display name for the color. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the color. |
| `value` | body | `string` | yes | The hex value for the color. |
