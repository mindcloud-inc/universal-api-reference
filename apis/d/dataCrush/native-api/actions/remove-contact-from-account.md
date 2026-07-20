# Remove Contact From Account with DataCrush

Removes a contact from an account in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/account/contact-delete`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Remove Contact From Account](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_key` | body | `string` | yes | Account key to update. |
| `contact_key` | body | `string` | yes | Existing contact key to remove. |
