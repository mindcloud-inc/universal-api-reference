# Export Form Analytics with Florm

Creates an export task for Florm form analytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/export/form/analytics`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Export Form Analytics](https://api.florm.io/docs#/default/export_analytics_form_v1_export_form_analytics_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Export file type. |
| `form_guid` | body | `string` | yes | GUID of the Florm form to export analytics for. |
