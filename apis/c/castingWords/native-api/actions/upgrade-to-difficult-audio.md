# Upgrade To Difficult Audio with CastingWords

Updates a CastingWords order to difficult audio.

## Endpoint

- **Method:** `POST`
- **Path:** `audiofile/:audiofile_id/upgrade`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Upgrade To Difficult Audio](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audiofile_id` | path | `string` | yes | CastingWords audiofile ID. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test upgrade. |
