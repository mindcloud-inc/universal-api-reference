# City of Beverly Hills: Native API Reference

A consolidated summary of City of Beverly Hills's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://opendata-hub.beverlyhills.org/
- **API base URL:** `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`

## Authentication

### Public Access

Public ArcGIS data; no credentials required.

This API does not require request authentication.

[Official authentication documentation](https://developers.arcgis.com/rest/services-reference/enterprise/get-started-with-the-services-directory/)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Layer](actions/get-feature-layer.md) | `GET :serviceName/FeatureServer/:layerId` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/layer-feature-service/) |
| [Get Feature Service](actions/get-feature-service.md) | `GET :serviceName/FeatureServer` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/feature-service/) |
| [List Services](actions/list-services.md) | `GET services` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/get-started-with-the-services-directory/) |
| [Query Features](actions/query-features.md) | `GET :serviceName/FeatureServer/:layerId/query` | [docs](https://developers.arcgis.com/rest/services-reference/enterprise/query-feature-service-layer/) |
