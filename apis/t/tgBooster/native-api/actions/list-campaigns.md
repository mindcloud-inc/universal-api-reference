# List Campaigns with TgBooster

Retrieves campaigns from a specific TgBooster cabinet.

## Endpoint

- **Method:** `POST`
- **Path:** `/cabinet/{CabinetId}/companies`
- **Base URL:** `https://api.tgbooster.ru/api`
- **Official documentation:** [List Campaigns](https://tgbooster.gitbook.io/tgbooster/api/api-metody#poluchenie-spiska-kampanii-s-vozmozhnostyu-filtracii-statistiki)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CabinetId` | path | `number` | yes | Cabinet ID returned by List Cabinets. |
| `filters[start_date]` | body | `date` | no | Start date for campaign statistics filtering. |
| `filters[finish_date]` | body | `date` | no | Finish date for campaign statistics filtering. |
