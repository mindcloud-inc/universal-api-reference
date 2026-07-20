# Enrich Location with Zoominfo

Enriches a location with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/location`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Location](https://api-docs.zoominfo.com/#2b221ad0-f6c2-40cb-b721-6513e90afd8d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | no | The id of the parent company for which you want to find locations |
