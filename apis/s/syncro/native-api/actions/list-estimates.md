# List Estimates with Syncro

Retrieves a list of estimates from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Estimates](https://api-docs.syncromsp.com/#/Estimate/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mine` | query | `boolean` | no |
| `status` | query | `string` | no |
| `page` | query | `number` | no |
