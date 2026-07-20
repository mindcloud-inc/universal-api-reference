# List Sales Stock Levels with HirePOS

Retrieves sales stock levels from HirePOS as a CSV feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/API/SalesStockLevels`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [List Sales Stock Levels](https://docs.hirepos.com/en/articles/8667457)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Code` | query | `string` | yes | HirePOS subscription code for the sales stock feed. |
| `Recalc` | query | `string` | no | Set True to recalculate quantity in stock in real time. This may impact performance. |
