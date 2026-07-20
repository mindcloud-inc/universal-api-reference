# List Entity with CoordinateHQ

## Endpoint

- **Method:** `GET`
- **Path:** `/entity`
- **Base URL:** `https://app.coordinatehq.com/api/v1`
- **Official documentation:** [List Entity](https://app.coordinatehq.com/static/API_Documentation.html#entity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_dt` | query | `string` | yes |
| `end_dt` | query | `string` | no |
| `entity` | query | `list<string>` | no |
| `sort` | query | `list<string>` | no |
