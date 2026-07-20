# Order Transcript With Speaker Names with CastingWords

Creates a transcript order with speaker names in CastingWords.

## Endpoint

- **Method:** `POST`
- **Path:** `order_url`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Order Transcript With Speaker Names](https://castingwords.com/docs/developer/SimpleAPI.html#order_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public audio or video URL to transcribe. |
| `names[]` | body | `array<string>` | yes | Known speaker names for the transcript. Send multiple values as a array. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test order. |
