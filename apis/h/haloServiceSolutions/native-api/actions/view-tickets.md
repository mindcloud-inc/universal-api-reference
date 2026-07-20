# View Tickets with Halo Service Solutions

Retrieves tickets from a Halo Service Solutions ticket view.

## Endpoint

- **Method:** `POST`
- **Path:** `/Tickets/View`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [View Tickets](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `[]` | body | `array<object>` | yes | Array of ticket objects to view. |
| `[].id` | body | `number` | yes | Ticket ID inside the request array. |
