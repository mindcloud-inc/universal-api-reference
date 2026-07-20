# Create Design with Canva

Creates a new design in Canva.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/designs`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Create Design](https://www.canva.dev/docs/connect/api-reference/designs/create-design/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `design_type` | body | `object` | no | The design type to create. |
| `design_type.type` | body | `list` | yes | Choose whether the new design uses a preset type or custom dimensions. Accepted values: `custom`, `preset`. |
| `design_type.name` | body | `list` | no | Preset Canva design type name. Accepted values: `doc`, `presentation`, `whiteboard`. |
| `design_type.width` | body | `number` | no | Width in pixels for a custom design type. |
| `design_type.height` | body | `number` | no | Height in pixels for a custom design type. |
| `asset_id` | body | `string` | no | Optional asset ID to insert into the created design. |
| `title` | body | `string` | no | Optional title for the new design. Maximum length: 255. |
