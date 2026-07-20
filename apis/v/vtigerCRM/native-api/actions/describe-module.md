# Describe Module with Vtiger CRM

Retrieves module metadata from Vtiger CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/describe`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Describe Module](https://vtap.vtiger.com/platform/rest-apis.html#describe---module-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `elementType` | query | `string` | yes | Vtiger module name such as Contacts, Accounts, or Leads. |
