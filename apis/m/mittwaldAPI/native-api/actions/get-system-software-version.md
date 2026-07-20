# Get System Software Version with mittwald

Retrieves system software version from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/system-softwares/:systemSoftwareId/versions/:systemSoftwareVersionId`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get System Software Version](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `systemSoftwareId` | path | `string` | yes | The unique identifier of the system software. |
| `systemSoftwareVersionId` | path | `string` | yes | The unique identifier of the system software version. |
