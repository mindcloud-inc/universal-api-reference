# Get operations reserve report with MoySklad

Retrieves the operations reserve report from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `report/byoperations/reserve`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get operations reserve report](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-po-dokumentam-nomenklatury)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | MoySklad filter argument. |
