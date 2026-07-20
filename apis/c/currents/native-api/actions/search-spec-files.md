# Search Spec Files with Currents

## Endpoint

- **Method:** `GET`
- **Path:** `/spec-files/:projectId`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [Search Spec Files](https://docs.currents.dev/resources/api/api-resources/spec-files)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date_end` | query | `string` | yes |
| `date_start` | query | `string` | yes |
| `projectId` | path | `string` | yes |
| `specNameFilter` | query | `string` | yes |
