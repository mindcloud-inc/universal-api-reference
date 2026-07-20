# Update Multistep Test with PageVitals

## Endpoint

- **Method:** `PUT`
- **Path:** `/:websiteId/multistep/:testId`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Update Multistep Test](https://pagevitals.com/docs/rest-api/reference/multistep/detail/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `websiteId` | path | `string` | yes |
| `testId` | path | `string` | yes |
| `alias` | body | `string` | no |
| `device` | body | `string` | no |
