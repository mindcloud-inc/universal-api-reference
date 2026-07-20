# List Ticket Interactions with Octadesk

Retrieves interactions for an Octadesk ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:number/interactions`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Ticket Interactions](https://developers.octadesk.com/reference/getticketinteractions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handlers` | query | `boolean` | no | Return only handler interactions |
| `number` | path | `string` | yes | Ticket number |
