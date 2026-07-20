# Snooze Issue with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/:id/snooze/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Snooze Issue](https://developers.intruder.io/reference/issues_snooze_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Intruder issue identifier. |
| `reason` | body | `string` | yes | Why the issue is being snoozed. |
| `details` | body | `string` | no | Optional extra context for the snooze. |
| `duration` | body | `number` | no | How long to snooze the issue. |
| `duration_type` | body | `string` | no | The unit for the snooze duration. |
