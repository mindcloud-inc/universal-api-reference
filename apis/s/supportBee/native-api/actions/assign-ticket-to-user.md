# Assign Ticket to User with SupportBee

Assigns a SupportBee ticket to a user.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/user_assignment`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Assign Ticket to User](https://supportbee.com/docs/api/reference#tag/Users/paths/~1tickets~1{id}~1user_assignment/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
| `user_assignment.user_id` | body | `number` | yes | SupportBee user ID to assign. |
