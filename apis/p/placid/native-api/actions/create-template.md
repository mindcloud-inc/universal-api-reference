# Create Template with Placid

Creates a new template in Placid.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/templates`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Create Template](https://placid.app/docs/2.0/rest/templates#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title for the new template. |
| `from_template` | body | `string` | no | Existing template UUID to clone from. |
| `width` | body | `number` | no | Template width in pixels when creating from scratch. |
| `height` | body | `number` | no | Template height in pixels when creating from scratch. |
| `tags[]` | body | `array<string>` | no | Tags to attach to the template. |
| `custom_data` | body | `object` | no | Custom data to store on the template. |
| `add_to_collections[]` | body | `array<string>` | no | Collection UUIDs that should include the new template. |
