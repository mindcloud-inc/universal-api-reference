# Create Live Workshop with TrainerCentral

Creates a live workshop in TrainerCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Create Live Workshop](https://help.trainercentral.com/portal/en/kb/articles/create-a-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session.name` | body | `string` | yes | The name of the live workshop. |
| `session.description` | body | `string` | no | Optional description for the live workshop. |
| `session.scheduledTime` | body | `number` | yes | Live workshop start time in milliseconds. |
| `session.scheduledEndTime` | body | `number` | yes | Live workshop end time in milliseconds. |
| `session.timezone` | body | `string` | yes | IANA timezone for the scheduled start and end times. |
