# Create Item with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/item`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Item](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/item#create-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Item name. |
| `Type` | body | `string` | yes | QuickBooks item type. |
| `IncomeAccountRef.value` | body | `string` | yes | Income account ID required when creating a service item in QuickBooks. |
