# List System Software Versions with mittwald

Retrieves system software versions from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/system-softwares/:systemSoftwareId/versions`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List System Software Versions](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `systemSoftwareId` | path | `string` | yes | The system software ID. |
