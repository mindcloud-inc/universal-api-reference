# Enrich Hashtags with Zoominfo

Enriches company hashtags with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/hashtag`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Hashtags](https://api-docs.zoominfo.com/#886fb5cc-b587-4f26-bd68-892798d45ffe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | no | The id of the company for which you want to view hashtags |
