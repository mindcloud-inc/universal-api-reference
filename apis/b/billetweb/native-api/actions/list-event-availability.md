# List Event Availability with Billetweb

Retrieves availability for a Billetweb event.

## Endpoint

- **Method:** `GET`
- **Path:** `/event/:id/avail`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List Event Availability](https://www.billetweb.fr/bo/api.php#/api/event/:id/avail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier. |
| `temp` | query | `boolean` | no | Include baskets currently in progress. |
| `past` | query | `boolean` | no | Include past sessions. |
| `session` | query | `string` | no | Specific session identifier or unique start time. |
