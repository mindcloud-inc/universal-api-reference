# Join Storm with Stormboard

Joins a Storm in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/storms/join`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Join Storm](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stormid` | body | `number` | yes | Storm ID from the Stormboard share dialog. |
| `stormkey` | body | `string` | yes | Private storm key from the Stormboard share dialog. |
