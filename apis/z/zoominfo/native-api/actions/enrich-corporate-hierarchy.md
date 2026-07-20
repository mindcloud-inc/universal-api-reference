# Enrich Corporate Hierarchy with Zoominfo

Enriches a corporate hierarchy with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/corporatehierarchy`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Corporate Hierarchy](https://api-docs.zoominfo.com/#1bf83184-9ee9-478f-b839-9afab4dfe18e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matchCompanyInput[]` | body | `array<object>` | yes | Array of company match objects for corporate hierarchy enrich. The collection example uses `companyName`. |
| `outputFields[]` | body | `array<string>` | no | Array of response field names to return. Send multiple values as a array. |
