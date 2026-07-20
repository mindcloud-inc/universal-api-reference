# Export All Statistics with Sipuni

Exports all call recording entries from Sipuni.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistic/export/all`
- **Base URL:** `https://sipuni.com/api`
- **Official documentation:** [Export All Statistics](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum 200000 rows per page. |
| `order` | query | `string` | no | Use asc to count from earliest rows or desc from latest rows. |
| `page` | query | `string` | no | — |
