# List Quote Items with EenvoudigFactureren

Retrieves quote items from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/quotes/:quote_id/items`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [List Quote Items](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381985-api-offertes)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quote_id` | path | `string` | yes | EenvoudigFactureren quote ID. |
