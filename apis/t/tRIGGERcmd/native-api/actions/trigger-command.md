# Trigger Command with TRIGGERcmd

Triggers a command on a computer in TRIGGERcmd.

## Endpoint

- **Method:** `POST`
- **Path:** `/run/trigger`
- **Base URL:** `https://www.triggercmd.com/api`
- **Official documentation:** [Trigger Command](https://docs.triggercmd.com/#/API/TriggerCommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computer` | body | `string` | yes | The computer name to target. |
| `trigger` | body | `string` | yes | The trigger name of the command to run. |
| `params` | body | `string` | no | Optional text to pass to the command. |
