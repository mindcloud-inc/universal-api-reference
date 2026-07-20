# Get DNS Records with GoDaddy CRM

Retrieves DNS records for a GoDaddy domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains/:domain/records/:type/:name`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Get DNS Records](https://developer.godaddy.com/doc/endpoint/domains)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Required domain whose DNS records should be retrieved |
| `type` | path | `string` | yes | Required DNS record type |
| `name` | path | `string` | yes | Required DNS record name |
