# Get money plot series report with MoySklad

Retrieves the money plot series report from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `report/money/plotseries`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get money plot series report](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-dengi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | MoySklad interval argument. |
| `momentFrom` | query | `string` | yes | MoySklad momentFrom argument. |
| `momentTo` | query | `string` | yes | MoySklad momentTo argument. |
