# Update Template with Placid

Updates an existing template in Placid.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/rest/templates/:templateUuid`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Update Template](https://placid.app/docs/2.0/rest/templates#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateUuid` | path | `string` | yes | UUID of the template to update. |
| `title` | body | `string` | no | Updated title for the template. |
| `tags[]` | body | `array<string>` | no | Updated tags for the template. |
| `custom_data` | body | `object` | no | Updated custom data for the template. |
