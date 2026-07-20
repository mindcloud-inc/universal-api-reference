# Replace All DNS Records with GoDaddy CRM

Replaces all DNS records for a GoDaddy domain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/domains/:domain/records`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Replace All DNS Records](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Required domain whose DNS records should be replaced |
| `records[].type` | body | `string` | yes | Required DNS record type |
| `records[].name` | body | `string` | yes | Required DNS record name |
| `records[].data` | body | `string` | yes | Required DNS record data |
