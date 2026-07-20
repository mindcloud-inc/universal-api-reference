# Get Domain Registration Schema with GoDaddy CRM

Retrieves a domain registration schema from GoDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/domains/register/schema/:tld`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Get Domain Registration Schema](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `tld` | path | `string` | yes | The top-level domain whose registration schema should be retrieved. |
