# Create Planned Run Skip Overrides with Rachio Smart Hose Timer

Creates planned run skip overrides in Rachio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://cloud-rest.rach.io/program/createPlannedRunSkipOverrides`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Create Planned Run Skip Overrides](https://rachio.readme.io/reference/programservice_createplannedrunskipoverrides)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `plannedRunId` | body | `string` | yes |
| `date` | body | `object` | yes |
