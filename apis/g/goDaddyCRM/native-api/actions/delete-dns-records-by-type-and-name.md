# Delete DNS Records By Type And Name with GoDaddy CRM

Deletes DNS records from a GoDaddy domain.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/domains/:domain/records/:type/:name`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Delete DNS Records By Type And Name](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Required domain whose DNS records should be deleted |
| `type` | path | `string` | yes | Required DNS record type to delete |
| `name` | path | `string` | yes | Required DNS record name to delete |
