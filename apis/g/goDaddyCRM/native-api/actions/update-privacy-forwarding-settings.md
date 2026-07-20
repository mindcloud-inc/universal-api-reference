# Update Privacy Forwarding Settings with GoDaddy CRM

Updates privacy forwarding settings for a GoDaddy domain.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/customers/:customerId/domains/:domain/privacy/forwarding`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Update Privacy Forwarding Settings](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Required customer identifier who owns the domain |
| `domain` | path | `string` | yes | Required domain whose privacy forwarding should be updated |
| `privateEmailType` | body | `string` | yes | Required private email type |
| `emailPreference` | body | `string` | yes | Required forwarding preference |
| `forwardingEmail` | body | `string` | no | Optional forwarding destination email |
