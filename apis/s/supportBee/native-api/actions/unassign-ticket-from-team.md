# Unassign Ticket from Team with SupportBee

Unassigns a SupportBee ticket from its team.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id/team_assignment`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Unassign Ticket from Team](https://supportbee.com/docs/api/reference#tag/Teams/paths/~1tickets~1{id}~1team_assignment/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
