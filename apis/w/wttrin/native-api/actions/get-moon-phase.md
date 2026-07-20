# Get Moon Phase with wttr.in

Retrieves the moon phase for a date from wttr.in.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:moonDate]`
- **Base URL:** `https://wttr.in`
- **Official documentation:** [Get Moon Phase](https://github.com/chubin/wttr.in#moon-phases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moonDate` | path | `string` | yes | Moon phase path segment in wttr.in syntax, such as Moon@2026-04-30. |
