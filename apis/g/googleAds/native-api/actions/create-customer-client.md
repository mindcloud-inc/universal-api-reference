# Create Customer Client with Google Ads

Creates a customer client in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:createCustomerClient`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Create Customer Client](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerService/CreateCustomerClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Manager customer ID under which the child account will be created (without dashes). |
| `customerClient` | body | `object` | yes | Customer client settings for the new child account. |
| `customerClient.descriptiveName` | body | `string` | yes | Display name for the new child customer account. |
| `customerClient.currencyCode` | body | `string` | yes | ISO 4217 currency code for the new account, for example USD. |
| `customerClient.timeZone` | body | `string` | yes | IANA time zone for the new account, for example America/New_York. |
| `validateOnly` | body | `boolean` | no | When true, validates request without creating the account. |
