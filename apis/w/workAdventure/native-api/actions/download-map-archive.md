# Download map archive with WorkAdventure

Downloads a directory archive from WorkAdventure map storage.

## Endpoint

- **Method:** `GET`
- **Path:** `https://mindcloud-34294.map-storage.workadventu.re/download`
- **Base URL:** `https://admin.workadventu.re`
- **Official documentation:** [Download map archive](https://github.com/workadventure/workadventure/tree/develop/map-storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directory` | query | `string` | yes | Directory to archive. Use ./ for the root. |
