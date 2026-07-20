# Create Escalation Policy with Better Stack Uptime

Creates a new escalation policy in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/policies`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Create Escalation Policy](https://betterstack.com/docs/uptime/api/create-escalation-policy/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Escalation policy name. |
| `steps[0].wait_before` | body | `number` | yes | Seconds to wait before running the first step. |
| `steps[0].instructions_comment` | body | `string` | yes | Instructions text for the first step. |
| `steps[0].instructions_reminder_enabled` | body | `boolean` | no | Whether to keep reminding for the instruction step. |
| `team_name` | body | `string` | no | Better Stack team name when required by the token scope. |
