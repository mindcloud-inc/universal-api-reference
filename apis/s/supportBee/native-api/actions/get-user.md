# Get User with SupportBee

Retrieves a user or customer group from SupportBee.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Get User](https://supportbee.com/docs/api/reference#tag/Users/paths/~1users~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee user ID. |
| `max_tickets` | query | `number` | no | Maximum number of related tickets to include. |
