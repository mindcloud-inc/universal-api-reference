# Get operations stock report with MoySklad

Retrieves the operations stock report from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `report/byoperations/stock`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get operations stock report](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-po-dokumentam-nomenklatury)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | MoySklad filter argument. |
