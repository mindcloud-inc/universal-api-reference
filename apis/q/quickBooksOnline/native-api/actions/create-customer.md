# Create Customer with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/customer`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Customer](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/customer#create-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DisplayName` | body | `string` | yes | Customer display name. |
