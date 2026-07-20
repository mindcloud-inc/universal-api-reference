# RUIAN: Native API Reference

A consolidated summary of RUIAN's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://developers.arcgis.com/rest/services-reference/enterprise/map-service/
- **API base URL:** `https://ags.cuzk.gov.cz/arcgis/rest/services/RUIAN/MapServer`

## Authentication

### Public VDP

Public VDP access with no registration

This API does not require request authentication.

[Official authentication documentation](https://ruian.cuzk.cz/)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get all layers and tables](actions/get-all-layers-and-tables.md) | `GET /layers` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/all-layers-and-tables/) |
| [Get layer details](actions/get-layer-details.md) | `GET /{layerId}` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/layer-table/) |
| [Get service details](actions/get-service-details.md) | `GET /` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/get-started-with-the-services-directory/) |
| [Query layer features](actions/query-layer-features.md) | `GET /{layerId}/query` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/query-map-service-layer/) |
