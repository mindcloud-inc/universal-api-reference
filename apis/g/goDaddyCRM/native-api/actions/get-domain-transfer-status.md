# Get Domain Transfer Status with GoDaddy CRM

Retrieves domain transfer status from GoDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/domains/:domain/transfer`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Get Domain Transfer Status](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `domain` | path | `string` | yes | Domain name whose transfer status should be retrieved. |
