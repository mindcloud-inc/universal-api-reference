# Search Accounts with DataCrush

Finds accounts in DataCrush by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/search`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Search Accounts](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Search accounts by name. |
