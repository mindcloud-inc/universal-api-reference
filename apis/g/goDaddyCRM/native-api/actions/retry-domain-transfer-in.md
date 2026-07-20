# Retry Domain Transfer In with GoDaddy CRM

Retries a domain transfer into GoDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/customers/:customerId/domains/:domain/transferInRetry`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Retry Domain Transfer In](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `domain` | path | `string` | yes | The domain name to retry the transfer for. |
| `authCode` | body | `string` | yes | The authorization code for transferring the domain. |
