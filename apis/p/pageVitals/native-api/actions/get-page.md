# Get Page with PageVitals

## Endpoint

- **Method:** `GET`
- **Path:** `/:websiteId/pages/:pageId`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Get Page](https://pagevitals.com/docs/rest-api/reference/pages/page-detail/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The internal ID of the website. |
| `pageId` | path | `string` | yes | The internal ID of the page. |
| `device` | query | `string` | yes | The device profile to query, such as desktop or mobile. |
