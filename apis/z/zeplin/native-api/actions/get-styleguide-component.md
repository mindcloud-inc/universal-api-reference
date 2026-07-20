# Get Styleguide Component with Zeplin

Retrieves a styleguide component from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/components/{component_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Styleguide Component](https://docs.zeplin.dev/reference/getstyleguidecomponent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `component_id` | path | `string` | yes | Component id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
| `include_latest_version` | query | `boolean` | no | Whether to include the latest version data in the Component object |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
