# Create Account with Vtiger CRM

Creates a new account in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Accounts`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Account](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON object string for the Account fields to create. |
