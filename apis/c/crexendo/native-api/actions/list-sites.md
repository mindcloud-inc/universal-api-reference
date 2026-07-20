# List Sites with Crexendo

Retrieves sites for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/sites`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Sites](https://docs.ns-api.com/reference/get_domains-domain-sites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
