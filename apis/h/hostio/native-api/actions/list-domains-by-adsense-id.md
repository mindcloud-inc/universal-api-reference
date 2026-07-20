# List Domains by AdSense ID with Host.io

Finds domains in Host.io by AdSense ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/adsense/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by AdSense ID](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Google AdSense publisher ID to search for. |
