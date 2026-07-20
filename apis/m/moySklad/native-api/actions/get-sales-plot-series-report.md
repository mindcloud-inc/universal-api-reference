# Get sales plot series report with MoySklad

Retrieves the sales plot series report from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `report/sales/plotseries`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get sales plot series report](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-pokazateli-prodazh-i-zakazow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | MoySklad interval argument. |
| `momentFrom` | query | `string` | yes | MoySklad momentFrom argument. |
| `momentTo` | query | `string` | yes | MoySklad momentTo argument. |
