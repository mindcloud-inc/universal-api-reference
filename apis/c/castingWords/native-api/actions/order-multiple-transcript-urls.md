# Order Multiple Transcript URLs with CastingWords

Creates transcript orders from multiple URLs in CastingWords.

## Endpoint

- **Method:** `POST`
- **Path:** `order_url`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Order Multiple Transcript URLs](https://castingwords.com/docs/developer/SimpleAPI.html#order_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url[]` | body | `array<string>` | yes | Public audio or video URLs to transcribe. Send multiple values as a array. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test order. |
