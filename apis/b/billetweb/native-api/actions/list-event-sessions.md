# List Event Sessions with Billetweb

Retrieves sessions for a Billetweb event.

## Endpoint

- **Method:** `GET`
- **Path:** `/event/:id/dates`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [List Event Sessions](https://www.billetweb.fr/bo/api.php#/api/event/:id/dates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier. |
| `past` | query | `boolean` | no | Include past sessions. |
| `last_update` | query | `number` | no | Only return sessions updated after this Unix timestamp. |
| `disabled` | query | `number` | no | Filter by visibility state. |
| `past_by` | query | `number` | no | Include sessions ended within the last X days. |
| `start_from` | query | `number` | no | Filter from this session start Unix timestamp. |
| `start_to` | query | `number` | no | Filter until this session start Unix timestamp. |
