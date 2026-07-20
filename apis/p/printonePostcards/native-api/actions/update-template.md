# Update Template with Print.one Postcards

Updates an existing template in Print.one Postcards.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/templates/[:id]`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Update Template](https://api.print.one/docs/v2#operation/Template/updateTemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Template ID. |
| `name` | body | `string` | yes | New template name. |
