# Add DNS Records with GoDaddy CRM

Adds DNS records to a GoDaddy domain.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/domains/:domain/records`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Add DNS Records](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Required domain whose DNS records should be augmented |
| `records[].type` | body | `string` | yes | Required DNS record type |
| `records[].name` | body | `string` | yes | Required DNS record name |
| `records[].data` | body | `string` | yes | Required DNS record data |
