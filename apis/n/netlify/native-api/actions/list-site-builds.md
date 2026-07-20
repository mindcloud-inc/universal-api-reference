# List Site Builds with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/builds`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [List Site Builds](https://open-api.netlify.com/#operation/listSiteBuilds)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes |
