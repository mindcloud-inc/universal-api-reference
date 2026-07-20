# Update Team with Onfleet

Updates an existing team in Onfleet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/:teamId`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Update Team](https://docs.onfleet.com/reference/update-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The Onfleet team ID. |
| `name` | body | `string` | no | A unique name for the team. |
| `workers[]` | body | `array<string>` | no | An array of worker IDs. |
| `managers[]` | body | `array<string>` | no | An array of managing administrator IDs. |
| `hub` | body | `string` | no | Optional. The ID of the team's hub. |
| `enableSelfAssignment` | body | `boolean` | no | Whether team self-assignment is enabled. |
