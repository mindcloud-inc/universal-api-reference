# Get turnover by store report with MoySklad

Retrieves the turnover by store report from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `report/turnover/bystore`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get turnover by store report](https://dev.moysklad.ru/doc/api/remap/1.2/reports/#otchety-otchet-oboroty)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | MoySklad filter argument. |
