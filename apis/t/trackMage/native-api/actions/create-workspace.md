# Create Workspace with TrackMage

Creates a new workspace in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Create Workspace](https://docs.trackmage.com/docs/workspaces.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `team.name` | body | `string` | yes |
| `title` | body | `string` | yes |
| `defaultTrackingPage` | body | `object` | yes |
| `preferredCarriers[]` | body | `array<string>` | no |
| `considerShipmentDelayed` | body | `object` | no |
| `workflowsOrder[]` | body | `array<string>` | no |
| `logo` | body | `string` | no |
| `emailSettings.logo` | body | `string` | no |
| `emailSettings.signature` | body | `string` | no |
| `emailSettings.smtpCredentials` | body | `string` | no |
