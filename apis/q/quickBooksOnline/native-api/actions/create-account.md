# Create Account with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/account`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Account](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/account#create-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Account name. |
| `AccountType` | body | `string` | yes | QuickBooks account type. |
