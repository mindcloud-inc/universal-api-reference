# Create Template with Print.one Postcards

Creates a new template in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/templates`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Create Template](https://api.print.one/docs/v2#operation/Template/createTemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Template name. |
| `format` | body | `string` | yes | Template format. |
| `labels[]` | body | `array<string>` | yes | Labels attached to this template. |
| `pages[]` | body | `array<object>` | yes | Template pages as an array of objects with content. |
| `options` | body | `object` | no | Template options. |
| `overlay` | body | `string` | yes | Postal overlay. |
