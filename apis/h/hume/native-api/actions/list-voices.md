# List voices with Hume

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/tts/voices`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [List voices](https://dev.hume.ai/reference/voices/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `provider` | query | `list` | yes | Voice provider to list. HUME_AI returns shared Voice Library voices; CUSTOM_VOICE returns custom voices in the account. Accepted values: `0`, `1`. |
| `ascending_order` | query | `boolean` | no | When true, returns voices in ascending order. |
| `filter_tag` | query | `string` | no | Filter voices by tag using TAG:TAG_VALUE syntax, for example GENDER:Male. Send multiple values as a array. |
