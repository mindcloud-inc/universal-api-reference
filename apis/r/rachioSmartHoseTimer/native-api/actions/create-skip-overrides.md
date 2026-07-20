# Create Skip Overrides with Rachio Smart Hose Timer

Creates program skip overrides in Rachio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://cloud-rest.rach.io/program/createSkipOverrides`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [Create Skip Overrides](https://rachio.readme.io/reference/programservice_createskipoverrides)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `programId` | body | `string` | yes |
| `timestamp` | body | `date` | yes |
