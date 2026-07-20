# Unassign Ticket from User with SupportBee

Unassigns a SupportBee ticket from its user.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tickets/:id/user_assignment`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Unassign Ticket from User](https://supportbee.com/docs/api/reference#tag/Users/paths/~1tickets~1{id}~1user_assignment/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
