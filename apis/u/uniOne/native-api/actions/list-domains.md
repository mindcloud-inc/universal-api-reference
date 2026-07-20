# List Domains with UniOne

Retrieves domains from UniOne, optionally by exact domain.

## Endpoint

- **Method:** `POST`
- **Path:** `domain/list.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [List Domains](https://docs.unione.io/en/web-api-ref#domain-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | Optional exact domain name to filter the list. |
