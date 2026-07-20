# List Domain Addresses with Crexendo

Retrieves addresses for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/addresses`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Domain Addresses](https://docs.ns-api.com/reference/getaddressesfordomain)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
