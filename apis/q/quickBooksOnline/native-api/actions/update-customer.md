# Update Customer with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Update Customer](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/customer#full-update-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Customer Id to update. |
| `SyncToken` | body | `string` | yes | Current QuickBooks SyncToken for optimistic locking. |
| `DisplayName` | body | `string` | yes | Updated customer display name. |
