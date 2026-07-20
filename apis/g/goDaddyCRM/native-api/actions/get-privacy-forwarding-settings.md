# Get Privacy Forwarding Settings with GoDaddy CRM

Retrieves privacy forwarding settings for a GoDaddy domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/domains/:domain/privacy/forwarding`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Get Privacy Forwarding Settings](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Required customer identifier who owns the domain |
| `domain` | path | `string` | yes | Required domain whose privacy forwarding settings should be retrieved |
