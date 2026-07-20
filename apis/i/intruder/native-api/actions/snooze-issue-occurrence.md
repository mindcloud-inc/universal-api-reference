# Snooze Issue Occurrence with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/:issueId/occurrences/:id/snooze/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Snooze Issue Occurrence](https://developers.intruder.io/reference/issues_occurrences_snooze_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `string` | yes | The Intruder issue identifier. |
| `id` | path | `string` | yes | The Intruder occurrence identifier. |
| `reason` | body | `string` | yes | Why the occurrence is being snoozed. |
| `details` | body | `string` | no | Optional extra context for the snooze. |
| `duration` | body | `number` | no | How long to snooze the occurrence. |
| `duration_type` | body | `string` | no | The unit for the snooze duration. |
