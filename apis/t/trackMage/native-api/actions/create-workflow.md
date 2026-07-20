# Create Workflow with TrackMage

Creates a new workflow in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Create Workflow](https://docs.trackmage.com/docs/workflow/workflow.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | — |
| `type` | body | `string` | yes | — |
| `workspace` | body | `string` | yes | — |
| `credentials.type` | body | `string` | no | — |
| `credentials.team` | body | `string` | no | — |
| `notificationEmails[]` | body | `array<string>` | no | — |
| `enabled` | body | `boolean` | yes | — |
| `period` | body | `string` | yes | applies only to out |
| `integration` | body | `object` | no | — |
| `firstTimeSetupPassed` | body | `boolean` | no | — |
