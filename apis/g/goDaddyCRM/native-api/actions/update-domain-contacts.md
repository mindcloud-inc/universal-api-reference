# Update Domain Contacts with GoDaddy CRM

Updates contacts for a GoDaddy domain.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/customers/:customerId/domains/:domain/contacts`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Update Domain Contacts](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Required customer identifier who owns the domain |
| `domain` | path | `string` | yes | Required domain whose contacts should be updated |
| `identityDocumentId` | body | `string` | no | Optional identity document associated with the registrant update |
