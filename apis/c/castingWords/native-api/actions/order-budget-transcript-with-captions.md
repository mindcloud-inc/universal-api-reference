# Order Budget Transcript With Captions with CastingWords

Creates a budget transcript order with captions in CastingWords.

## Endpoint

- **Method:** `POST`
- **Path:** `order_url`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Order Budget Transcript With Captions](https://castingwords.com/docs/developer/SimpleAPI.html#order_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public audio or video URL to transcribe. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test order. |
