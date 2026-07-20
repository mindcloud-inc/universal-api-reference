# Export Project with Resco Cloud

Exports an app project definition from Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExportProject`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Export Project](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$id` | query | `string` | no | Project ID to export. Use either Project ID or Project Name. |
| `$name` | query | `string` | no | Project name to export. Use either Project Name or Project ID. |
