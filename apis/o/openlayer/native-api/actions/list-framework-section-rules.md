# List Framework Section Rules with Openlayer

Retrieves rules for a framework section in Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/frameworks/:frameworkId/sections/:sectionId/rules`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [List Framework Section Rules](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frameworkId` | path | `string` | yes | Openlayer framework ID. |
| `sectionId` | path | `string` | yes | Openlayer framework section ID. |
