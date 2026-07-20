# List Content Types with Flotiq

Retrieves content types from your Flotiq project.

## Endpoint

- **Method:** `GET`
- **Path:** `/internal/contenttype`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [List Content Types](https://flotiq.com/docs/API/content-type/listing-ctd/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter content types by name. |
