# List NFe Events V2 with Qive

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/nfe/events`
- **Base URL:** `https://sandbox-api.arquivei.com.br`
- **Official documentation:** [List NFe Events V2](https://developers.qive.com.br/docs/get/v2/nfe/events)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_key` | query | `string` | yes | NFe access key whose events should be returned. |
| `type[]` | query | `array<string>` | no | Optional event types to filter by. |
