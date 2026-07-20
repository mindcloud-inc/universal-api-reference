# Delete Participants with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/delete-participants`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Delete Participants](https://runsignup.com/API/race/:race_id/delete-participants/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `allow_non_imports` | body | `string` | no | — |
| `request` | body | `string` | yes | — |
