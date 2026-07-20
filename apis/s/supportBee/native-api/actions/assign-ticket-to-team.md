# Assign Ticket to Team with SupportBee

Assigns a SupportBee ticket to a team.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/team_assignment`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Assign Ticket to Team](https://supportbee.com/docs/api/reference#tag/Teams/paths/~1tickets~1{id}~1team_assignment/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
| `team_assignment.team_id` | body | `number` | yes | SupportBee team ID to assign. |
