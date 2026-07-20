# List NFe Manifests V2 with Qive

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/nfe/manifest`
- **Base URL:** `https://sandbox-api.arquivei.com.br`
- **Official documentation:** [List NFe Manifests V2](https://developers.qive.com.br/docs/get/v2/nfe/manifest)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_key[]` | query | `array<string>` | yes | NFe access keys to retrieve manifest information for. |
