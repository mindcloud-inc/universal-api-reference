# List Attributes with Sertifier

Finds attributes in Sertifier by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/attribute/search`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [List Attributes](https://sertifier.docs.apiary.io/reference/attribute/search-attributes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | body | `string` | no | Filter attributes by title. |
| `types[]` | body | `array<number>` | no | Optional attribute type filters. |
