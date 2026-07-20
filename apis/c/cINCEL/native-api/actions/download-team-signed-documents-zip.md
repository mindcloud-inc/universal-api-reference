# Download Team Signed Documents ZIP with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/:takeout.zip`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Download Team Signed Documents ZIP](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/-takeout-.zip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `takeout` | path | `string` | yes | Year or year-month period, for example `2026` or `2026-04`. |
