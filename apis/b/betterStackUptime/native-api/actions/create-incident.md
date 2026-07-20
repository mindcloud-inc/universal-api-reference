# Create Incident with Better Stack Uptime

Creates a new incident in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/incidents`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Create Incident](https://betterstack.com/docs/uptime/api/create-a-new-incident/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `summary` | body | `string` | yes | Short incident summary shown in Better Stack. |
| `requester_email` | body | `string` | no | Email address of the incident reporter. |
| `description` | body | `string` | no | Detailed incident description. |
| `name` | body | `string` | no | Optional incident name. |
| `call` | body | `boolean` | no | Enable phone call notifications. |
| `sms` | body | `boolean` | no | Enable SMS notifications. |
| `email` | body | `boolean` | no | Enable email notifications. |
| `critical_alert` | body | `boolean` | no | Mark the incident as critical. |
| `team_wait` | body | `number` | no | Seconds to wait before escalating to the team. |
| `policy_id` | body | `string` | no | Escalation policy ID to apply to the incident. |
| `team_name` | body | `string` | no | Better Stack team name when required by the token scope. |
