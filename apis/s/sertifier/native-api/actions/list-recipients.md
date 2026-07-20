# List Recipients with Sertifier

Finds recipients in Sertifier by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/recipient/search`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [List Recipients](https://sertifier.docs.apiary.io/reference/recipient/search-recipients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startIndex` | body | `number` | no |
| `length` | body | `number` | no |
| `searchTerm` | body | `string` | no |
