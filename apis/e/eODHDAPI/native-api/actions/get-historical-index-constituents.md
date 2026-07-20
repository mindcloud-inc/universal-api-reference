# Get Historical Index Constituents with EODHD

Retrieves historical index constituents from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/fundamentals/{indexSymbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Historical Index Constituents](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `indexSymbol` | path | `string` | yes | EODHD index symbol, such as `GSPC.INDX`. |
| `from` | query | `date` | no | Start date in `YYYY-MM-DD` format. |
| `to` | query | `date` | no | End date in `YYYY-MM-DD` format. |
