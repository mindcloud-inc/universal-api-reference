# List Site Submissions with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/submissions`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [List Site Submissions](https://open-api.netlify.com/#operation/listSiteSubmissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `string` | yes |
