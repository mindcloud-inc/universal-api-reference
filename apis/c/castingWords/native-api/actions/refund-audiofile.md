# Refund Audiofile with CastingWords

Updates a CastingWords audiofile by issuing a refund.

## Endpoint

- **Method:** `POST`
- **Path:** `audiofile/:audiofile_id/refund`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Refund Audiofile](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidrefund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audiofile_id` | path | `string` | yes | CastingWords audiofile ID. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test refund. |
