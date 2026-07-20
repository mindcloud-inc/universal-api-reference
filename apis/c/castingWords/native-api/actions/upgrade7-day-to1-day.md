# Upgrade 7-Day To 1-Day with CastingWords

Updates a 7-day CastingWords order to 1-day service.

## Endpoint

- **Method:** `POST`
- **Path:** `audiofile/:audiofile_id/upgrade`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Upgrade 7-Day To 1-Day](https://castingwords.com/docs/developer/SimpleAPI.html#audiofileidupgrade)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audiofile_id` | path | `string` | yes | CastingWords audiofile ID. |
| `test` | body | `string` | no | Set to 1 to run a CastingWords test upgrade. |
