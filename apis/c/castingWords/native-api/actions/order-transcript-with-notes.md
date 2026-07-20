# Order Transcript With Notes with CastingWords

Creates a transcript order with notes in CastingWords.

## Endpoint

- **Method:** `POST`
- **Path:** `order_url`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Order Transcript With Notes](https://castingwords.com/docs/developer/SimpleAPI.html#order_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public audio or video URL to transcribe. |
| `notes` | body | `string` | yes | Instructions for the transcriber. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test order. |
