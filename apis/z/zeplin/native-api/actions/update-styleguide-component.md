# Update Styleguide Component with Zeplin

Updates an existing styleguide component in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/styleguides/{styleguide_id}/components/{component_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Styleguide Component](https://docs.zeplin.dev/reference/updatestyleguidecomponent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `component_id` | path | `string` | yes | Component id |
| `description` | body | `string` | yes | New description for component |
