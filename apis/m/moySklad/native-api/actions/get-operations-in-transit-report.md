# Get operations in transit report with MoySklad

Retrieves the operations in transit report from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `report/byoperations/intransit`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get operations in transit report](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-po-dokumentam-nomenklatury)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | MoySklad filter argument. |
