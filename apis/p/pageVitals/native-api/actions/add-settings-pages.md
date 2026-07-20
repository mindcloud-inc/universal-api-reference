# Add Settings Pages with PageVitals

## Endpoint

- **Method:** `POST`
- **Path:** `/:websiteId/settings/pages`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Add Settings Pages](https://pagevitals.com/docs/rest-api/reference/settings/pages/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `websiteId` | path | `string` | yes |
| `input[].url` | body | `string` | yes |
| `input[].alias` | body | `string` | no |
