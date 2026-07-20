# Create Multistep Test with PageVitals

## Endpoint

- **Method:** `POST`
- **Path:** `/:websiteId/multistep`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Create Multistep Test](https://pagevitals.com/docs/rest-api/reference/multistep/list/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `websiteId` | path | `string` | yes |
| `alias` | body | `string` | no |
| `device` | body | `string` | no |
