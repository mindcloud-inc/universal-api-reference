# Update Account with DataCrush

Updates an existing account in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/update`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Update Account](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_key` | body | `string` | yes | Account key to update. |
| `name` | body | `string` | no | Updated account name. |
