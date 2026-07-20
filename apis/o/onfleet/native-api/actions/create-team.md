# Create Team with Onfleet

Creates a new team in Onfleet.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Create Team](https://docs.onfleet.com/reference/create-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A unique name for the team. |
| `workers[]` | body | `array<string>` | no | An array of worker IDs. |
| `managers[]` | body | `array<string>` | no | An array of managing administrator IDs. |
| `hub` | body | `string` | no | Optional. The ID of the team's hub. |
| `enableSelfAssignment` | body | `boolean` | no | Whether team self-assignment is enabled. |
