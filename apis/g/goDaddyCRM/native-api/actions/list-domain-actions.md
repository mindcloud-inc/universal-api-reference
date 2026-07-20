# List Domain Actions with GoDaddy CRM

Retrieves actions for a GoDaddy domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/domains/:domain/actions`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [List Domain Actions](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Required customer identifier who owns the domain |
| `domain` | path | `string` | yes | Required domain whose recent actions should be listed |
