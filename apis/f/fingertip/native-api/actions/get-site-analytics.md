# Get Site Analytics with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/sites/:siteId/analytics`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Get Site Analytics](https://docs.fingertip.com/openapi-specs/get-comprehensive-site-analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeStore` | query | `string` | no | Include store analytics data |
| `period` | query | `string` | no | Time period for analytics data |
| `siteId` | path | `string` | yes | ID of the site to get analytics for |
