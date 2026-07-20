# Get Layer with City of Beverly Hills

Retrieves feature layer details from City of Beverly Hills.

## Endpoint

- **Method:** `GET`
- **Path:** `:serviceName/FeatureServer/:layerId`
- **Base URL:** `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`
- **Official documentation:** [Get Layer](https://developers.arcgis.com/rest/services-reference/enterprise/layer-feature-service/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layerId` | path | `string` | yes | Layer identifier within the FeatureServer. |
| `serviceName` | path | `string` | yes | ArcGIS service folder or service name. |
