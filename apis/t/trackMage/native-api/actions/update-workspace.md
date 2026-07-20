# Update Workspace with TrackMage

Updates an existing workspace in TrackMage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workspaces/{id}`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Update Workspace](https://docs.trackmage.com/docs/workspaces.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource identifier |
| `title` | body | `string` | yes | — |
| `defaultTrackingPage` | body | `object` | yes | — |
| `preferredCarriers[]` | body | `array<string>` | no | — |
| `considerShipmentDelayed` | body | `object` | no | — |
| `workflowsOrder[]` | body | `array<string>` | no | — |
| `logo` | body | `string` | no | — |
| `emailSettings.logo` | body | `string` | no | — |
| `emailSettings.signature` | body | `string` | no | — |
| `emailSettings.smtpCredentials` | body | `string` | no | — |
