# List Check Downtimes with updown.io

Retrieves all check downtimes from updown.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/checks/:token/downtimes`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [List Check Downtimes](https://updown.io/api#GET-/api/checks/:token/downtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page to fetch, 100 per page. |
| `results` | query | `boolean` | no | Include detailed downtime results. |
| `token` | path | `string` | yes | The check unique token. |
