# Get Styleguide Component Latest Version with Zeplin

Retrieves the latest styleguide component version from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/components/{component_id}/versions/latest`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Styleguide Component Latest Version](https://docs.zeplin.dev/reference/getstyleguidecomponentlatestversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `component_id` | path | `string` | yes | Component id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
