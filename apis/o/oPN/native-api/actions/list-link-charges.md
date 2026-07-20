# List Link Charges with OPN

Retrieves a list of charges for a link from OPN.

## Endpoint

- **Method:** `GET`
- **Path:** `/links/:id/charges`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [List Link Charges](https://docs.omise.co/links-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The link ID whose charges to list. |
