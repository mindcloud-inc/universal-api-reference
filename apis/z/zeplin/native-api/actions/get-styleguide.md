# Get Styleguide with Zeplin

Retrieves a styleguide from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Styleguide](https://docs.zeplin.dev/reference/getstyleguide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
