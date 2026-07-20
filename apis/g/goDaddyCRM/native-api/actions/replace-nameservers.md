# Replace Nameservers with GoDaddy CRM

Replaces nameservers for a GoDaddy domain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/customers/:customerId/domains/:domain/nameServers`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Replace Nameservers](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Required customer identifier who owns the domain |
| `domain` | path | `string` | yes | Required domain whose nameservers should be replaced |
| `nameServers[]` | body | `string<string>` | yes | Required list of replacement nameservers Send multiple values as a array. |
