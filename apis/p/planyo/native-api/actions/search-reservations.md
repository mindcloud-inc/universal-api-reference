# Search Reservations with Planyo

Finds reservations in Planyo by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.planyo.com/rest`
- **Official documentation:** [Search Reservations](https://www.planyo.com/api.php?topic=reservation_search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `detail_level` | query | `number` | no |
| `sort` | query | `string` | no |
