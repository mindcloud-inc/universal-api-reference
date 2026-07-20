# Update Customer Information with Pinghome

Updates existing customer information in Pinghome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customer-cmd/v1/customer`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Customer Information](https://docs.pinghome.io/customer-account-management/account-settings/update-customer-information/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The updated first name of the customer. |
| `surname` | body | `string` | no | The updated surname of the customer. |
