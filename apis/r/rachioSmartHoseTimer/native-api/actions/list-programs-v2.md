# List Programs V2 with Rachio Smart Hose Timer

Retrieves program records from your Rachio account.

## Endpoint

- **Method:** `GET`
- **Path:** `https://cloud-rest.rach.io/program/listProgramsV2`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [List Programs V2](https://rachio.readme.io/reference/programservice_listprogramsv2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resourceId.baseStationId` | query | `string` | no |
| `resourceId.valveId` | query | `string` | no |
