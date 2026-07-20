# Get team memberships with Asana

Retrieves team memberships from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `team_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get team memberships](https://developers.asana.com/reference/getteammemberships)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no |
| `team` | query | `string` | no |
| `user` | query | `string` | no |
| `workspace` | query | `string` | no |
