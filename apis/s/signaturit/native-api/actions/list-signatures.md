# List Signatures with Signaturit

Retrieves signatures from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/signatures.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Signatures](https://docs.signaturit.com/api/latest#signatures_get_signatures)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of signatures to return. |
| `offset` | query | `number` | no | Results offset. |
