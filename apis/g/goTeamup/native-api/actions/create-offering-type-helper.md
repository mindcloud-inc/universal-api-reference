# Create Offering Type Helper with GoTeamup

Creates a new offering type in GoTeamup.

## Endpoint

- **Method:** `POST`
- **Path:** `/offering_types`
- **Base URL:** `https://goteamup.com/api/v2`
- **Official documentation:** [Create Offering Type Helper](https://docs.goteamup.com/api-reference/endpoints/offering-types-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | yes |
| `schedule_type` | body | `string` | yes |
