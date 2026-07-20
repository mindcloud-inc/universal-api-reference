# List Files with Pinata

Retrieves files from Pinata for a selected network.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/files/:network`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [List Files](https://docs.pinata.cloud/api-reference/endpoint/list-files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network` | path | `string` | yes | Network to list files from (`private` or `public`). |
