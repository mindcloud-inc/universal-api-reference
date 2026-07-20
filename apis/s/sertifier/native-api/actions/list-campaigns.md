# List Campaigns with Sertifier

Finds campaigns in Sertifier by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/search`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [List Campaigns](https://sertifier.docs.apiary.io/reference/campaign/search-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startIndex` | body | `number` | no | — |
| `length` | body | `number` | no | — |
| `status[]` | body | `array<number>` | no | Send multiple values as a array. |
| `searchTerm` | body | `string` | no | — |
